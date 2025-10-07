## `percona:psmdb-8.0.12`

```console
$ docker pull percona@sha256:f36a3ebab210daa632bbde4cd5bc5afc06d9c14b52d68a9042b45d7744bf6a9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0.12` - linux; amd64

```console
$ docker pull percona@sha256:b490c371eeaf5ca8437ed6a7a050101fb042117a58e55ac2d6557e28ddbbf0d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291777397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e4e4daf7617a1774076fe813340f28cf5a5ecf2d6af6e0bfc38acbd63e9ffe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:36:47 GMT
ENV container oci
# Thu, 18 Sep 2025 08:36:48 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 18 Sep 2025 08:36:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:36:48 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:36:49 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 06 Oct 2025 13:56:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_VERSION=8.0.12-4
# Mon, 06 Oct 2025 13:56:56 GMT
ENV OS_VER=el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV FULL_PERCONA_VERSION=8.0.12-4.el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_REPO=testing
# Mon, 06 Oct 2025 13:56:56 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 06 Oct 2025 13:56:56 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV GOSU_VERSION=1.11
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
VOLUME [/data/db]
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 06 Oct 2025 13:56:56 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Oct 2025 13:56:56 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 06 Oct 2025 13:56:56 GMT
USER 1001
# Mon, 06 Oct 2025 13:56:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021eb52bd505473a29845a29d28668a7b0a5d28372fdbc5fbcdfda931040eab6`  
		Last Modified: Tue, 07 Oct 2025 17:40:04 GMT  
		Size: 8.4 MB (8399682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e7f1dd101e987e4077ef276705f2ff6810149a3ac3bfaf20d1d2fd5b1ef478`  
		Last Modified: Tue, 07 Oct 2025 17:42:48 GMT  
		Size: 242.8 MB (242776634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1fe7f88df839c72691ef0ceb177d0d4959ca0178de823aa08901b9352f591c`  
		Last Modified: Tue, 07 Oct 2025 17:40:22 GMT  
		Size: 1.7 KB (1665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0777d50ad30d696b10d4b9d27c1cc8304e883b8b735b94667c6b3aba9859f4`  
		Last Modified: Tue, 07 Oct 2025 17:39:39 GMT  
		Size: 4.1 KB (4068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399e9533d29d09a1ddebf1f1d5b028695cae0d417298face1ea42bbbbbab2292`  
		Last Modified: Tue, 07 Oct 2025 17:40:22 GMT  
		Size: 10.6 KB (10573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1189c5ddf25c6c7c0b30fa8dd7a8866be30a321435301cce27f7107412748f1d`  
		Last Modified: Tue, 07 Oct 2025 17:39:05 GMT  
		Size: 914.5 KB (914520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc8a7716413630d771ae98b8399416b956110f7ef8c037528e258a88138a739`  
		Last Modified: Tue, 07 Oct 2025 17:39:05 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cdb0f89aa77f2376c18ef1bd730c83afa684ec82e228145471c83a63f1ec4c`  
		Last Modified: Tue, 07 Oct 2025 17:39:05 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91bfebc81c3e3d29b9c7c157a1a7932d0020a3dae99d861a1c71d346faeb7ad`  
		Last Modified: Tue, 07 Oct 2025 17:39:05 GMT  
		Size: 4.8 KB (4843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0.12` - unknown; unknown

```console
$ docker pull percona@sha256:e3482dfb5a6eea7a402812669b5d00e9cfff07616e06a0b6a4b62fb8916e285c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092c173fdc041e4bf6297a4eaf578fb0b0f9d110537eea7b921edd85ef9573d1`

```dockerfile
```

-	Layers:
	-	`sha256:7335b79ea424f2164901cb20e39944fceed2dea8a00cc83aefb57c819b4f07ed`  
		Last Modified: Tue, 07 Oct 2025 20:10:27 GMT  
		Size: 32.6 KB (32558 bytes)  
		MIME: application/vnd.in-toto+json
