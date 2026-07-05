### Step 1 — Thicketry Event Schema v1.0  
**Placement:**
`/UMA/Geometry/Non-Dual-Hexeract/Auditing/Schemas/NDH-Thicketry-Event-Schema-v1.0.md`

#### 1. Core shape (every event)

```yaml
event_id:        string        # unique per event
trace_id:        string        # one per Thicketry run
timestamp:       string        # ISO-8601
step:            string        # one of 1..9 logical steps
phase:           string|null   # Detect/Protect/... when applicable
severity:        string        # INFO|WARN|ERROR|CRITICAL
category:        string        # GEOMETRY|DIVERGENCE|CONVERGENCE|BRAID|DENSITY|RESOLUTION|SPINE_BIND|TEMPORAL_BIND|PRODUCTION_BIND
payload:         object        # step-specific data
version:         string        # schema version, e.g. v1.0
```

---

#### 2. Step‑specific payloads

**Step 1 — Activate Thicketry Geometry**

```yaml
payload:
  geometry_version:  string
  seed_params:       object   # branching_factor, depth_limit, randomness_seed
  initial_nodes:     integer
  initial_edges:     integer
```

**Step 2 — Apply Divergence Rules**

```yaml
payload:
  rule_id:           string
  rule_version:      string
  node_id:           string
  pre_branch_factor: integer
  post_branch_factor:integer
  children_ids:      array[string]
```

**Step 3 — Apply Convergence Rules**

```yaml
payload:
  rule_id:           string
  rule_version:      string
  merged_node_ids:   array[string]
  target_node_id:    string
  convergence_success:boolean
```

**Step 4 — Apply Braid Logic**

```yaml
payload:
  rule_id:           string
  rule_version:      string
  path_ids:          array[string]
  braid_id:          string
  cycles_introduced: integer
  cycles_resolved:   integer
```

**Step 5 — Apply Tangle Density**

```yaml
payload:
  zone_id:           string
  density_value:     float
  density_threshold: float
  action_taken:      string   # PRESERVE|REDUCE|FLAG
```

**Step 6 — Resolve into Detect**

```yaml
payload:
  resolved_path_ids:   array[string]
  unresolved_path_ids: array[string]
  detect_input_id:     string
  resolution_success:  boolean
```

**Step 7 — Bind to Workflow Spine v1.1**

```yaml
payload:
  spine_run_id:       string
  binding_contract_id:string
  binding_success:    boolean
  error_code:         string|null
```

**Step 8 — Bind to Temporal Animation v1.1**

```yaml
payload:
  temporal_run_id:    string
  phase:              string   # Detect..Evolve
  expected_duration_s:float
  actual_duration_s:  float
  drift_ms:           integer
  binding_success:    boolean
```

**Step 9 — Bind to Production Order v1.3**

```yaml
payload:
  production_run_id:  string
  step_index:         integer  # should be 4 for Spine activation
  lineage_id:         string
  binding_success:    boolean
```

---

