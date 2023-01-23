# Guacamole setup on clean Ubuntu Server 20.04

## Requirements
1. JAVA `default-jre`
2. Tomcat
3. Database engine
4. Guacamole prerequisites:
    - Build essential `build-essential`
    - Maven - optional, when building client from source `maven`
    - Cairo `libcairo2-dev`
    - libjpeg-turbo `libjpeg-turbo8-dev`
    - libpng `libpng12-dev` - Ubuntu 20.04 `libpng12-0`
    - libtool `libtool-bin`
    - libuuid `uuid-dev`
    - Optional:
        - FFMpeg `libavcodec-dev libavformat-dev libavutil-dev libswscale-dev` 
        - FreeRDP `freerdp2-dev`
        - Pango (SSH, telnet) `libpango1.0-dev`
        - libssh2 `libssh2-1-dev`
        - libVNCServer `libvncserver-dev`
        - PulseAudio `libpulse-dev`
        - OpenSSL `libssl-dev`
        - libvorbis `libvorbis-dev`
        - libwebp `libwebp-dev`

## Install Guacamole
1. Download server source code
2. Configure, make & install
3. Start & enable `guacd` service
4. Create `/etc/guacamole` config directory & subdirectories
5. Download & setup WAR file
7. Set Guacamole home directory and add to tomcat config
8. Configure Guacamole server connections
9. Copy user-mapping file
10. Restart services

## Install LDAP integration
1. Add database authentication
    1. Install JDBC Connector
    2. Install Guacamole JDBC driver
    3. Create database
    4. Create users
    5. Configure Guacamole for database authentication
3. Prepare LDAP directory (optional)
4. Install LDAP extension
5. Configure Guacamole for LDAP Authentication