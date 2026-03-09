# `neo4j:2026.02.2-enterprise-ubi10`

## Docker Metadata

- Image ID: `sha256:04dd4052dbe010f8e53713e66f6d8347657b26d97ebe4197f21f987314130f85`
- Created: `2026-03-06T18:23:39.300882076Z`
- Virtual Size: ~ 795.47 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["tini","-g","--","/startup/docker-entrypoint.sh"]`
- Command: `["neo4j"]`
- Environment:
  - `PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `container=oci`
  - `NEO4J_SHA256=3edc16e54b70b190f460fed9a5eb31e7e4e8c6a52aa823bff6b18dd2d2183c8a`
  - `NEO4J_TARBALL=neo4j-enterprise-2026.02.2-unix.tar.gz`
  - `NEO4J_EDITION=enterprise`
  - `NEO4J_HOME=/var/lib/neo4j`
  - `LANG=C.UTF-8`
- Labels:
  - `architecture=x86_64`
  - `build-date=2026-03-02T08:55:38Z`
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
  - `org.opencontainers.image.created=2026-03-02T08:55:38Z`
  - `org.opencontainers.image.revision=22680d9fff6e4cead236be943e791fde5247c69a`
  - `release=1772441549`
  - `summary=Provides the latest release of the minimal Red Hat Universal Base Image 10.`
  - `url=https://catalog.redhat.com/en/search?searchType=containers`
  - `vcs-ref=22680d9fff6e4cead236be943e791fde5247c69a`
  - `vcs-type=git`
  - `vendor=Red Hat, Inc.`
  - `version=10.1`
