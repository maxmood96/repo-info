# `neo4j:2026.04.0-community-ubi10`

## Docker Metadata

- Image ID: `sha256:bd7ccc064096d4a2d3aa635585160b508c6cff6889cf6ffd34dc81f776ba477f`
- Created: `2026-05-05T23:11:15.06164809Z`
- Virtual Size: ~ 644.73 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["tini","-g","--","/startup/docker-entrypoint.sh"]`
- Command: `["neo4j"]`
- Environment:
  - `PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `container=oci`
  - `NEO4J_SHA256=fd750466b1247c0d1ef09a84c614f7e045793b30dfa277148e8da71646598820`
  - `NEO4J_TARBALL=neo4j-community-2026.04.0-unix.tar.gz`
  - `NEO4J_EDITION=community`
  - `NEO4J_HOME=/var/lib/neo4j`
  - `LANG=C.UTF-8`
- Labels:
  - `architecture=x86_64`
  - `build-date=2026-05-04T01:36:38Z`
  - `com.redhat.component=ubi10-minimal-container`
  - `com.redhat.license_terms=https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI`
  - `cpe=cpe:/o:redhat:enterprise_linux:10.1`
  - `description=The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly.`
  - `distribution-scope=public`
  - `io.buildah.version=1.42.2`
  - `io.k8s.description=The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly.`
  - `io.k8s.display-name=Red Hat Universal Base Image 10 Minimal`
  - `io.openshift.expose-services=`
  - `io.openshift.tags=minimal rhel10`
  - `maintainer=Red Hat, Inc.`
  - `name=ubi10/ubi-minimal`
  - `org.opencontainers.image.created=2026-05-04T01:36:38Z`
  - `org.opencontainers.image.revision=2c4967ab62628fff803457df7635994ca0e85fbc`
  - `release=1777858393`
  - `summary=Provides the latest release of the minimal Red Hat Universal Base Image 10.`
  - `url=https://catalog.redhat.com/en/search?searchType=containers`
  - `vcs-ref=2c4967ab62628fff803457df7635994ca0e85fbc`
  - `vcs-type=git`
  - `vendor=Red Hat, Inc.`
  - `version=10.1`
