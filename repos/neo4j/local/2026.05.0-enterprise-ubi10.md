# `neo4j:2026.05.0-enterprise-ubi10`

## Docker Metadata

- Image ID: `sha256:2efbfb70c41bad87a4ee4a912ff88c11d31c6eefb6863724d945df93b5f992a1`
- Created: `2026-06-15T23:16:35.912544993Z`
- Virtual Size: ~ 802.62 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["tini","-g","--","/startup/docker-entrypoint.sh"]`
- Command: `["neo4j"]`
- Environment:
  - `PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `container=oci`
  - `NEO4J_SHA256=2507ce15c1410931cf81db4435c1e1e437d5a857f59db3f946697988a5263aeb`
  - `NEO4J_TARBALL=neo4j-enterprise-2026.05.0-unix.tar.gz`
  - `NEO4J_EDITION=enterprise`
  - `NEO4J_HOME=/var/lib/neo4j`
  - `LANG=C.UTF-8`
- Labels:
  - `architecture=x86_64`
  - `build-date=2026-06-15T07:46:21Z`
  - `com.redhat.component=ubi10-minimal-container`
  - `com.redhat.license_terms=https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI`
  - `cpe=cpe:/o:redhat:enterprise_linux:10.2`
  - `description=The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly.`
  - `distribution-scope=public`
  - `io.buildah.version=1.42.2`
  - `io.k8s.description=The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly.`
  - `io.k8s.display-name=Red Hat Universal Base Image 10 Minimal`
  - `io.openshift.expose-services=`
  - `io.openshift.tags=minimal rhel10`
  - `maintainer=Red Hat, Inc.`
  - `name=ubi10/ubi-minimal`
  - `org.opencontainers.image.created=2026-06-15T07:46:21Z`
  - `org.opencontainers.image.revision=a079bd1cc91523a60704cf840463d737ba8b63de`
  - `release=1781509346`
  - `summary=Provides the latest release of the minimal Red Hat Universal Base Image 10.`
  - `url=https://catalog.redhat.com/en/search?searchType=containers`
  - `vcs-ref=a079bd1cc91523a60704cf840463d737ba8b63de`
  - `vcs-type=git`
  - `vendor=Red Hat, Inc.`
  - `version=10.2`
