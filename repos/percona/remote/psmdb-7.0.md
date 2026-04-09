## `percona:psmdb-7.0`

```console
$ docker pull percona@sha256:aa41970809f8c087165d8598c963cd968f7ba583bf2f29bee04ce0e4e18f4cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0` - linux; amd64

```console
$ docker pull percona@sha256:f1f637258f8d4a34736b2fe17579012bb1b957bcb5cecd336df0db0cc0274c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.2 MB (300194407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338fc2ad38a6c4821d4e73d8a53aa41465b3136dec3b2ae86005e27c2ab0bafd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:23:47 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Apr 2026 17:23:47 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Wed, 08 Apr 2026 17:23:47 GMT
ENV PSMDB_VERSION=7.0.31-17
# Wed, 08 Apr 2026 17:23:47 GMT
ENV OS_VER=el9
# Wed, 08 Apr 2026 17:23:47 GMT
ENV FULL_PERCONA_VERSION=7.0.31-17.el9
# Wed, 08 Apr 2026 17:23:47 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 08 Apr 2026 17:23:47 GMT
ENV PSMDB_REPO=release
# Wed, 08 Apr 2026 17:23:47 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Apr 2026 17:23:47 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Apr 2026 17:23:47 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Apr 2026 17:24:03 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Wed, 08 Apr 2026 17:24:03 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Wed, 08 Apr 2026 17:24:03 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Wed, 08 Apr 2026 17:24:03 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Wed, 08 Apr 2026 17:24:03 GMT
ENV GOSU_VERSION=1.11
# Wed, 08 Apr 2026 17:24:05 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Wed, 08 Apr 2026 17:24:05 GMT
VOLUME [/data/db]
# Wed, 08 Apr 2026 17:24:05 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Wed, 08 Apr 2026 17:24:06 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Wed, 08 Apr 2026 17:24:06 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Apr 2026 17:24:06 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:24:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Apr 2026 17:24:06 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 08 Apr 2026 17:24:06 GMT
USER 1001
# Wed, 08 Apr 2026 17:24:06 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fec4e3ba2497a613252e5571c10184b78ed722483394645ff8496a6a4f31bb`  
		Last Modified: Wed, 08 Apr 2026 17:24:39 GMT  
		Size: 8.8 MB (8843977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f53357bc4513beabd7fc1daa6d39b8d33b58b41bf8d935593ab6d087aa69943`  
		Last Modified: Wed, 08 Apr 2026 17:24:46 GMT  
		Size: 250.4 MB (250414940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1f7f3f93308aea592261b1eddf51b60015f249bb4902c995d31cd253b57a99`  
		Last Modified: Wed, 08 Apr 2026 17:24:38 GMT  
		Size: 1.7 KB (1666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e239411b0396d8349a200d04981f6bb1f399b10e2ca9a103b731d7ed65fe1d7`  
		Last Modified: Wed, 08 Apr 2026 17:24:40 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50934fdf3d8ba4ec99e94a3004c884294b7245bbb4b9153e89ecc4239595e39c`  
		Last Modified: Wed, 08 Apr 2026 17:24:40 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19ab7095c2e99c649dc9a1aedae3917a765820cb642730cec7acb8cd9922cc8`  
		Last Modified: Wed, 08 Apr 2026 17:24:41 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e39a207e1276d25100ff80e389c7360b7939934251440a9ddf34e624f63c5`  
		Last Modified: Wed, 08 Apr 2026 17:24:42 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec12a334e14c251048ba879275912758a2a8ecf9003bd3eeb3a83c5abb158c0`  
		Last Modified: Wed, 08 Apr 2026 17:24:42 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6896e3d913f19efbf3c340825f36e8569cad483eb0d8815ba486ef41b582731f`  
		Last Modified: Wed, 08 Apr 2026 17:24:43 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0` - unknown; unknown

```console
$ docker pull percona@sha256:3bfbd1b773b09cf64321d55455d5ac3dcdd685d2f3129ad4e01498af6eb26cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908a0b553964715afb729bb17430aae9ad42fc76be7de8ea3a97ad77a7dd4864`

```dockerfile
```

-	Layers:
	-	`sha256:e8515fd9c403fff02ff879e0b4ab092b17224095c46d20532fd6e2b04dc2f09a`  
		Last Modified: Wed, 08 Apr 2026 17:24:38 GMT  
		Size: 32.3 KB (32285 bytes)  
		MIME: application/vnd.in-toto+json
