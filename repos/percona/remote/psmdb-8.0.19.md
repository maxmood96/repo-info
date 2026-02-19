## `percona:psmdb-8.0.19`

```console
$ docker pull percona@sha256:2572872b5dd6d10c9ab2d8c4f855b2587cf92fef3148577b8db96dcdd93a9ae0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0.19` - linux; amd64

```console
$ docker pull percona@sha256:137dd1caa2eac2a9152795a8d73688abeac1799ff729c158fa3a3cfdc00f5267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308496989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7594bf5025457ffc2a1a314264a001af97164eedf81f6d6a2b6d80958115d374`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:42:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:42:46 GMT
COPY dir:a84da6f36b88f4eb0d6c411f65b34c1a9d85150d3035dd516db4ece0c2569465 in /      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:42:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:42:34Z" "org.opencontainers.image.created"="2026-02-17T16:42:34Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:42:34Z
# Thu, 19 Feb 2026 18:44:55 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 19 Feb 2026 18:44:55 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Thu, 19 Feb 2026 18:44:55 GMT
ENV PSMDB_VERSION=8.0.19-7
# Thu, 19 Feb 2026 18:44:55 GMT
ENV OS_VER=el9
# Thu, 19 Feb 2026 18:44:55 GMT
ENV FULL_PERCONA_VERSION=8.0.19-7.el9
# Thu, 19 Feb 2026 18:44:55 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 19 Feb 2026 18:44:55 GMT
ENV PSMDB_REPO=testing
# Thu, 19 Feb 2026 18:44:55 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Thu, 19 Feb 2026 18:44:55 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 19 Feb 2026 18:44:55 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 19 Feb 2026 18:44:55 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 19 Feb 2026 18:45:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Thu, 19 Feb 2026 18:45:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Thu, 19 Feb 2026 18:45:11 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Thu, 19 Feb 2026 18:45:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Thu, 19 Feb 2026 18:45:11 GMT
ENV GOSU_VERSION=1.11
# Thu, 19 Feb 2026 18:45:13 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Thu, 19 Feb 2026 18:45:13 GMT
VOLUME [/data/db]
# Thu, 19 Feb 2026 18:45:13 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Thu, 19 Feb 2026 18:45:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Thu, 19 Feb 2026 18:45:14 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 19 Feb 2026 18:45:14 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Thu, 19 Feb 2026 18:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Feb 2026 18:45:14 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 19 Feb 2026 18:45:14 GMT
USER 1001
# Thu, 19 Feb 2026 18:45:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4638e3415987f378f2d6dd70f9c6a2869dd5ebd09e3510ba45e46bbb6ec1a3dd`  
		Last Modified: Tue, 17 Feb 2026 18:08:54 GMT  
		Size: 40.0 MB (40033596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961845d964150992900ecce77b1abf27a42abf0cf24c28ade5f5b66b215498dd`  
		Last Modified: Thu, 19 Feb 2026 18:45:45 GMT  
		Size: 8.9 MB (8855421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c1f3e0fd2dac144f70f238691d8a9e011eeb4420c5168454856e495ca921d5`  
		Last Modified: Thu, 19 Feb 2026 18:45:51 GMT  
		Size: 258.7 MB (258655138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc86c469d82a32b4bfbebf0e588b40410f8f98bfaaae6078193be1f3e6cc361`  
		Last Modified: Thu, 19 Feb 2026 18:45:44 GMT  
		Size: 1.7 KB (1665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d02501aca77d3e51d94ace658b665df62eefe5bcf025742696f0c41002ebf`  
		Last Modified: Thu, 19 Feb 2026 18:45:45 GMT  
		Size: 4.1 KB (4070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada642c3e6f7262cf5fd5b05ba449a6ad6ad04f31d901e0ad85ef93da0896c3b`  
		Last Modified: Thu, 19 Feb 2026 18:45:46 GMT  
		Size: 10.6 KB (10574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05edb6327fe4d43f83492bd407f02ed5f7ff0e1a138272c9ea663c614297b6`  
		Last Modified: Thu, 19 Feb 2026 18:45:46 GMT  
		Size: 914.5 KB (914518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebafbb5c293cbbe748c43fc1f2bed0ff18858f905dffa1a4eb8053720b50a36d`  
		Last Modified: Thu, 19 Feb 2026 18:45:47 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da1f94257e23012be183e520ea90abd8f1cf386c3590c95da2635681857251f`  
		Last Modified: Thu, 19 Feb 2026 18:45:47 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5402ba879d7f9c0ca3ac48236c7a9509d88498c97f6c2d4febb1b68e6067a584`  
		Last Modified: Thu, 19 Feb 2026 18:45:47 GMT  
		Size: 4.8 KB (4843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0.19` - unknown; unknown

```console
$ docker pull percona@sha256:d999832fd9ba036d2f33539ffd67f3d3bfb993fea85614eb0fbb685ed78676e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afbb7a4adc7715b8a600f2de28f85d0918f677964c0a3e4864820404c9d9f981`

```dockerfile
```

-	Layers:
	-	`sha256:ed273b92d4172321ef83c547be7e5fb3ebc6a5382f918ecbff924fc38b60b19d`  
		Last Modified: Thu, 19 Feb 2026 18:45:45 GMT  
		Size: 32.6 KB (32575 bytes)  
		MIME: application/vnd.in-toto+json
