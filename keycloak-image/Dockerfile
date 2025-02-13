FROM quay.io/keycloak/keycloak:23.0.5 AS builder

# Enable health and metrics support
ENV KC_HEALTH_ENABLED=true
ENV KC_METRICS_ENABLED=true

WORKDIR /opt/keycloak

FROM quay.io/keycloak/keycloak:23.0.5
COPY --from=builder /opt/keycloak/ /opt/keycloak/
