FROM jboss/keycloak:7.0.0

# Set the Keycloak admin user and password
# ENV KEYCLOAK_USER=admin
# ENV KEYCLOAK_PASSWORD=admin
ENV REALM=sunbird

# Copy the custom login and email themes to the container
RUN mkdir -p /opt/jboss/keycloak/themes/$REALM
COPY artifacts/sunbird/email /opt/jboss/keycloak/themes/$REALM/email
COPY artifacts/sunbird/login /opt/jboss/keycloak/themes/$REALM/login

# COPY files/realm-export.json /tmp/realm-export.json
# COPY files/clients.json /tmp/clients.json
# COPY files/roles.json /tmp/roles.json

# Add Keycloak administrator user
# RUN /opt/jboss/keycloak/bin/add-user-keycloak.sh -r master -u keycloak -p keycloak

# Modify standalone.xml
# RUN sed -i 's/name="default"/name="standalone-ha"/' /opt/jboss/keycloak/standalone/configuration/standalone.xml

# CMD ["/opt/jboss/keycloak/bin/standalone.sh", "-b", "0.0.0.0", "-Dkeycloak.profile.feature.upload_scripts=enabled"]


EXPOSE 8080

# RUN curl -sS https://bootstrap.pypa.io/pip/2.7/get-pip.py -o get-pip.py
# RUN python get-pip.py
# RUN python setup.py install


# Start Keycloak server

# CMD ["bin/standalone.sh", "-b", "0.0.0.0"]