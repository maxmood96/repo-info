## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:0870e18e130809f2842f5d16f6b1d3a8a51dc2dfb7d9415a9dc970ce7d9909c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:058d4156f6bc6b073d7a1caf8171c915823ecd1054b7a18ee163bf746ff43ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255060467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7feb080f035ba49f631e8e836472a2dfea5f46805bdf816743a183358c467fce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 04 Dec 2025 19:46:05 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 04 Dec 2025 19:46:05 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Thu, 04 Dec 2025 19:46:05 GMT
ENV PSMDB_VERSION=6.0.25-20
# Thu, 04 Dec 2025 19:46:05 GMT
ENV OS_VER=el9
# Thu, 04 Dec 2025 19:46:05 GMT
ENV FULL_PERCONA_VERSION=6.0.25-20.el9
# Thu, 04 Dec 2025 19:46:05 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 04 Dec 2025 19:46:05 GMT
ENV PSMDB_REPO=release
# Thu, 04 Dec 2025 19:46:05 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 04 Dec 2025 19:46:05 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 04 Dec 2025 19:46:05 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 04 Dec 2025 19:46:18 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Thu, 04 Dec 2025 19:46:18 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Thu, 04 Dec 2025 19:46:18 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Thu, 04 Dec 2025 19:46:18 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Thu, 04 Dec 2025 19:46:18 GMT
ENV GOSU_VERSION=1.11
# Thu, 04 Dec 2025 19:46:20 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Thu, 04 Dec 2025 19:46:20 GMT
VOLUME [/data/db]
# Thu, 04 Dec 2025 19:46:20 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Thu, 04 Dec 2025 19:46:21 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Thu, 04 Dec 2025 19:46:21 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 04 Dec 2025 19:46:21 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:46:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Dec 2025 19:46:21 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 04 Dec 2025 19:46:21 GMT
USER 1001
# Thu, 04 Dec 2025 19:46:21 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c859cd48fb7ad420144e7068ecb5e0685f7c9ad6c1c6879debdd6006b98305`  
		Last Modified: Thu, 04 Dec 2025 19:46:56 GMT  
		Size: 8.8 MB (8815644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953e4d3fd8ee30190b7c580f50a9f6dfc2df06c7a4fd8d15a76e4f5bc6ef8af0`  
		Last Modified: Thu, 04 Dec 2025 21:11:48 GMT  
		Size: 205.3 MB (205251224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ed3237860f8e59ae077d672ff6acc91e158ddc2b4b763aeab1538c4fdd4173`  
		Last Modified: Thu, 04 Dec 2025 19:46:55 GMT  
		Size: 1.7 KB (1667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71437078b0678858ee883c6cd12a8f3c69227fb504d952bc5ce56fc69dc51c58`  
		Last Modified: Thu, 04 Dec 2025 19:46:55 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba891c2b06339a34583692b1270bd7846681c8205e544c5af3e2606151505534`  
		Last Modified: Thu, 04 Dec 2025 19:46:55 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5588f3069a6f3e706799704905e117ff9ee71d3c10969fa6297190b302701de9`  
		Last Modified: Thu, 04 Dec 2025 19:46:56 GMT  
		Size: 914.5 KB (914516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb280e9f316c57a9194ccb7aa9ec91a4660a13cf1a7418b84789a4b41b446711`  
		Last Modified: Thu, 04 Dec 2025 19:46:56 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1497f3ab06813959902fddd880d4e1c795231185c94d59c4841c9367afdb762`  
		Last Modified: Thu, 04 Dec 2025 19:46:56 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a0a412143cc4cd71f6720387fc6c205caaf5faff5944b97df001395695e9b7`  
		Last Modified: Thu, 04 Dec 2025 19:46:57 GMT  
		Size: 4.8 KB (4845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:9a29b71be2c36ac2aed89f3b7cd9f889cafbe82505249ea8e1ad12e2ecd60dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354d84dc6392097aa66ad6171eb5dade03621e5f70d169cae662025ca8514a54`

```dockerfile
```

-	Layers:
	-	`sha256:6c07f0cfdcfbd50d4dcc59f4378e5ada2dfe7ae6c6f3021a56600a64be3b0ca7`  
		Last Modified: Thu, 04 Dec 2025 21:11:17 GMT  
		Size: 32.8 KB (32778 bytes)  
		MIME: application/vnd.in-toto+json
