function ApplyDeepGateTightening(gates):
    g_S, g_SS, g_D = gates

    // tighten deep-gate tolerance
    if abs(g_D - 1) <= 0.015:
        return {g_S, g_SS, g_D}

    if abs(g_D - 1) <= 0.03:
        return {g_S, g_SS, g_D, "WARN"}

    return {g_S, g_SS, g_D, "FAIL"}
