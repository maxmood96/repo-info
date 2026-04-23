# `neo4j:2026.03.1-community-ubi10`

## Docker Metadata

- Image ID: `sha256:050ca8a08855b2395122c7abd5d6cd33dd2c14a25309e00254c3faa9e8c43527`
- Created: `2026-04-22T18:19:10.926432717Z`
- Virtual Size: ~ 649.25 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["tini","-g","--","/startup/docker-entrypoint.sh"]`
- Command: `["neo4j"]`
- Environment:
  - `PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `container=oci`
  - `NEO4J_SHA256=419c5a471a8b6918570da687215d7d3406983a6ae209fd3d96c2de2a90a5dcfb`
  - `NEO4J_TARBALL=neo4j-community-2026.03.1-unix.tar.gz`
  - `NEO4J_EDITION=community`
  - `NEO4J_HOME=/var/lib/neo4j`
  - `LANG=C.UTF-8`
- Labels:
  - `architecture=x86_64`
  - `build-date=2026-04-22T05:17:41Z`
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
  - `org.opencontainers.image.created=2026-04-22T05:17:41Z`
  - `org.opencontainers.image.revision=8f919d0175e713e927f4fc60c8a4a7f7d7d63a58`
  - `release=1776834797`
  - `summary=Provides the latest release of the minimal Red Hat Universal Base Image 10.`
  - `url=https://catalog.redhat.com/en/search?searchType=containers`
  - `vcs-ref=8f919d0175e713e927f4fc60c8a4a7f7d7d63a58`
  - `vcs-type=git`
  - `vendor=Red Hat, Inc.`
  - `version=10.1`
