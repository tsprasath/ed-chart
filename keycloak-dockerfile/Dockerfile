FROM jboss/keycloak:7.0.1

ENV REALM=sunbird

# Copy the custom login and email themes to the container
RUN mkdir -p /opt/jboss/keycloak/themes/$REALM
COPY artifacts/sunbird/email /opt/jboss/keycloak/themes/$REALM/email
COPY artifacts/sunbird/login /opt/jboss/keycloak/themes/$REALM/login
RUN mkdir -p /opt/jboss/keycloak/providers
COPY keycloak-email-phone-autthenticator-1.0-SNAPSHOT.jar /opt/jboss/keycloak/providers

EXPOSE 8080