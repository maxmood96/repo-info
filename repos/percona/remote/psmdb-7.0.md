## `percona:psmdb-7.0`

```console
$ docker pull percona@sha256:408a9f9f10805ede58da95b59ec83f6d49ae588dc967b7a44d68823cd45511cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0` - linux; amd64

```console
$ docker pull percona@sha256:ed260e21960f94e9515d8f6762a3ac0c2fc631ab68f639785f9c0d6df973e7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.2 MB (300225504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78223ce5eeb929d829c2150db1960e4db09818b85c5befc1a5bad50787f00d2a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:26:37 GMT
ENV container oci
# Mon, 13 Apr 2026 18:26:38 GMT
COPY dir:5191e1ce97881b91cd281225b61de5b907dbc286c69b6681e228608a9d6bab0b in /      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:26:38 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:39 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:26:26Z" "org.opencontainers.image.created"="2026-04-13T18:26:26Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:26:26Z
# Tue, 14 Apr 2026 20:45:26 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 14 Apr 2026 20:45:26 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Tue, 14 Apr 2026 20:45:26 GMT
ENV PSMDB_VERSION=7.0.31-17
# Tue, 14 Apr 2026 20:45:26 GMT
ENV OS_VER=el9
# Tue, 14 Apr 2026 20:45:26 GMT
ENV FULL_PERCONA_VERSION=7.0.31-17.el9
# Tue, 14 Apr 2026 20:45:26 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 14 Apr 2026 20:45:26 GMT
ENV PSMDB_REPO=release
# Tue, 14 Apr 2026 20:45:26 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 14 Apr 2026 20:45:26 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 14 Apr 2026 20:45:26 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 14 Apr 2026 20:45:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Tue, 14 Apr 2026 20:45:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Tue, 14 Apr 2026 20:45:43 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Tue, 14 Apr 2026 20:45:43 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Tue, 14 Apr 2026 20:45:43 GMT
ENV GOSU_VERSION=1.11
# Tue, 14 Apr 2026 20:45:45 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Tue, 14 Apr 2026 20:45:45 GMT
VOLUME [/data/db]
# Tue, 14 Apr 2026 20:45:45 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Tue, 14 Apr 2026 20:45:45 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Tue, 14 Apr 2026 20:45:45 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 14 Apr 2026 20:45:45 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:45:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Apr 2026 20:45:45 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 14 Apr 2026 20:45:45 GMT
USER 1001
# Tue, 14 Apr 2026 20:45:45 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b1ed13c5ef0ac6dbcd255a5c1be9e3c9c2903872aa4ae5fa877850a48fdaee26`  
		Last Modified: Mon, 13 Apr 2026 19:17:03 GMT  
		Size: 40.0 MB (40016560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87144286facd1f9e00c959a953c9442e5b518f0e1f20a72dd4a6aada74c5b7a9`  
		Last Modified: Tue, 14 Apr 2026 20:46:16 GMT  
		Size: 8.8 MB (8839882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f46059a3968813e650c33ba40d1d6f4547d6b91c992df0bcc397d3126b6425b`  
		Last Modified: Tue, 14 Apr 2026 20:46:20 GMT  
		Size: 250.4 MB (250416217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5fedfac09979d0b2c9ab136b63f112982bc07f80683a7880b64547e53a9830`  
		Last Modified: Tue, 14 Apr 2026 20:46:15 GMT  
		Size: 1.7 KB (1665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7393733672497cf4aa80af39bf198702fc17b96d99e0de264521516c3524afb4`  
		Last Modified: Tue, 14 Apr 2026 20:46:15 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538390eeab32f028ab2fc7b559f339608798776f6454195f8b6c04e900beb3bd`  
		Last Modified: Tue, 14 Apr 2026 20:46:17 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0897c5f4c7823cea9146bce95f1f0ed96043533021e710e588ae2e7db66889f1`  
		Last Modified: Tue, 14 Apr 2026 20:46:17 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b86e27ae752cdce62f243da8312c9624854ebe326de3e0a815109f0cf72f179`  
		Last Modified: Tue, 14 Apr 2026 20:46:17 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e34fb00e9528afc201727b004f9b300a9b4923737583494faf20a1b4870283`  
		Last Modified: Tue, 14 Apr 2026 20:46:18 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc369659ca7f407da937cba9da33712bfece4d8df8b3a90a72db2984738883f`  
		Last Modified: Tue, 14 Apr 2026 20:46:18 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0` - unknown; unknown

```console
$ docker pull percona@sha256:736eb1b868ae915ea0825f2cfd38a3ea8db194de1fdbeda8101867db141cfa4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b07a8bec5cf886abe3794703897c66602e4db249496eaf58751cd078963f334`

```dockerfile
```

-	Layers:
	-	`sha256:9ad45b792201901d34acdc0a39e3412007995e572b466cf357ed1c73762721a3`  
		Last Modified: Tue, 14 Apr 2026 20:46:15 GMT  
		Size: 32.3 KB (32285 bytes)  
		MIME: application/vnd.in-toto+json
