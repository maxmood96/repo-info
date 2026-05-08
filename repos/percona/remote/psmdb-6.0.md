## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:5d7a06c247f826b2603525dd568e057c08a51d5674d673a926992ca3af0bcd78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:9ad85335d832a3c64c15e5a3060644c9c5a11571633664f8cb8157271a525589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269288152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c4135cbad3bc77c2b41aebfbecb5fec2658b1027b50b7622f2d7e871d72dc3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 06 May 2026 12:56:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:56:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:56:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:56:14 GMT
ENV container oci
# Wed, 06 May 2026 12:56:14 GMT
COPY dir:4c4996e917f33023b976824d7cb68c72b897d6d36b90e718143d5c6b6644b5f2 in /      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:56:15 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:03Z" "org.opencontainers.image.created"="2026-05-06T12:56:03Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:03Z
# Fri, 08 May 2026 16:20:05 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 May 2026 16:20:05 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Fri, 08 May 2026 16:20:05 GMT
ENV PSMDB_VERSION=6.0.27-21
# Fri, 08 May 2026 16:20:05 GMT
ENV OS_VER=el9
# Fri, 08 May 2026 16:20:05 GMT
ENV FULL_PERCONA_VERSION=6.0.27-21.el9
# Fri, 08 May 2026 16:20:05 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 08 May 2026 16:20:05 GMT
ENV PSMDB_REPO=release
# Fri, 08 May 2026 16:20:05 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 May 2026 16:20:05 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 May 2026 16:20:05 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 May 2026 16:20:18 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Fri, 08 May 2026 16:20:18 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Fri, 08 May 2026 16:20:18 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Fri, 08 May 2026 16:20:18 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Fri, 08 May 2026 16:20:18 GMT
ENV GOSU_VERSION=1.11
# Fri, 08 May 2026 16:20:20 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Fri, 08 May 2026 16:20:20 GMT
VOLUME [/data/db]
# Fri, 08 May 2026 16:20:20 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Fri, 08 May 2026 16:20:20 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Fri, 08 May 2026 16:20:20 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Fri, 08 May 2026 16:20:20 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 16:20:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 16:20:20 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 08 May 2026 16:20:20 GMT
USER 1001
# Fri, 08 May 2026 16:20:20 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:df0edd575569e5cb7e2e34f252e4cf36c13679e9633d7c97be861b8b247c70bc`  
		Last Modified: Wed, 06 May 2026 13:26:44 GMT  
		Size: 40.0 MB (39994775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0ea6fe197bd53d00392182f4583843afdde84905acd772ec9e7c3b2bb3e188`  
		Last Modified: Fri, 08 May 2026 16:20:47 GMT  
		Size: 8.8 MB (8838700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa8d8482adb536e35c9b08b4c6a77f263cabd8c2fd8afdb2c4e5fd2a70cc786`  
		Last Modified: Fri, 08 May 2026 16:20:51 GMT  
		Size: 219.5 MB (219501832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00819666d3642b39bde1eb5f140657047aa5a0d22da51a2bb4bce0e61bb32004`  
		Last Modified: Fri, 08 May 2026 16:20:46 GMT  
		Size: 1.7 KB (1668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edd3b704388111cab559defd064ab06e3c0e5924ebce11580b5f2f49b30ed2e`  
		Last Modified: Fri, 08 May 2026 16:20:46 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd7178083edb0a9ee20a254e411e70a3be12f2a64792d133a34d565c56ef94d`  
		Last Modified: Fri, 08 May 2026 16:20:48 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20918340cbc665e92e7e0b43230a863cbc2eba21f3cc7a2fb48404a84b2d3619`  
		Last Modified: Fri, 08 May 2026 16:20:48 GMT  
		Size: 914.5 KB (914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6203c3ae72eaf535e133f7a31523799454448642bfb8607293302a67b4161a39`  
		Last Modified: Fri, 08 May 2026 16:20:49 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b61723471445f338fbbaef5be0f8920ee3c50f0adf02ef1619815b2c6daac3b`  
		Last Modified: Fri, 08 May 2026 16:20:49 GMT  
		Size: 4.0 KB (3961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b04a37fcf56df6cd596f8521c42ebb4b11612c00a8e7563c89ae4a3f2938f78`  
		Last Modified: Fri, 08 May 2026 16:20:49 GMT  
		Size: 4.8 KB (4845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:540a77f5141866f65acbc569c53ef0f7b271690dbd9d3a52f713f89a1771a603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c783dd4036d3746946ffc04d2e1fb22a1c15018b16d5b0c3432ffec97ff379b`

```dockerfile
```

-	Layers:
	-	`sha256:6193de63508540b90cab12211be1c54673d0b6b95a910084c7016c0d434a8ffc`  
		Last Modified: Fri, 08 May 2026 16:20:46 GMT  
		Size: 32.8 KB (32778 bytes)  
		MIME: application/vnd.in-toto+json
