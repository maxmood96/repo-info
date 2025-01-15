## `percona:8-centos`

```console
$ docker pull percona@sha256:26f681b8ebd151076c0fd824fab662c9c8a8e932ae46bdce485fcd3c0e732da0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:7dacd5705acfb1b304e25b6269b48389185d11521a6f50c8c38d266121df0fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385934106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589abd9c09b22398eb517dcdb4820537bc191502770cbe4244204394a9771527`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL url="https://www.redhat.com"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Jan 2025 11:00:36 GMT
ENV container oci
# Wed, 08 Jan 2025 11:00:36 GMT
COPY dir:ca56c4399f153561fdce7628edce358895393e72057424065cc9920dd3bc2dfc in / 
# Wed, 08 Jan 2025 11:00:36 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["/bin/bash"]
# Wed, 08 Jan 2025 11:00:36 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL "build-date"="2025-01-09T06:40:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Wed, 08 Jan 2025 11:00:36 GMT
RUN /bin/sh
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 08 Jan 2025 11:00:36 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_VERSION=8.0.40-31.1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV OS_VER=el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_PERCONA_VERSION=8.0.40-31.1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.40-1.el9
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_REPO=testing
# Wed, 08 Jan 2025 11:00:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.40-31-1
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 08 Jan 2025 11:00:36 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 08 Jan 2025 11:00:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 08 Jan 2025 11:00:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 08 Jan 2025 11:00:36 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Wed, 08 Jan 2025 11:00:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Jan 2025 11:00:36 GMT
USER mysql
# Wed, 08 Jan 2025 11:00:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Tue, 14 Jan 2025 20:37:28 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Tue, 14 Jan 2025 20:34:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de979cc62c2560860a82998c8121d11d640141616841b341c33e5cc9b27c60e6`  
		Last Modified: Sat, 11 Jan 2025 01:29:47 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a72f07cae8d459b50e0259f177b9b4a3584ed7341db5983d12103648a648a2`  
		Last Modified: Sat, 11 Jan 2025 01:29:47 GMT  
		Size: 8.3 MB (8336345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef412e132d16dcadfd328db67195efcc375f36c2bc833b54ab9ae0eda497fedc`  
		Last Modified: Sat, 11 Jan 2025 01:29:51 GMT  
		Size: 338.2 MB (338155210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1b043ca95a8067ae983dd69c58f51741d737f2f38a540f8d17df53b80f3e7b`  
		Last Modified: Tue, 14 Jan 2025 20:37:27 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ab8dd7d16ed8b141c31a1b8c95ab63392796071d846891d027ef26f6a245e2`  
		Last Modified: Tue, 14 Jan 2025 20:37:28 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a602ffebef6334b515c3b46bbdd7f09759db0ddb2dac414727e032ac7dd5f50`  
		Last Modified: Sat, 11 Jan 2025 01:29:48 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8-centos` - unknown; unknown

```console
$ docker pull percona@sha256:db3ff463dba4862195a8dd56cd70ed8edb0de7f68a57f6d35f60e187f283131f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b286d4c1bcd15cb6a9c83b9b7f077f87aa6fe395138c887ddd285ccb548c438`

```dockerfile
```

-	Layers:
	-	`sha256:e9a2407c6de20b5ab4e221cd167203866ead05a89f444735df62a95ba4f5848b`  
		Last Modified: Wed, 15 Jan 2025 00:27:10 GMT  
		Size: 31.9 KB (31925 bytes)  
		MIME: application/vnd.in-toto+json
