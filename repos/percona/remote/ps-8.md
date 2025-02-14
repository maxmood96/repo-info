## `percona:ps-8`

```console
$ docker pull percona@sha256:5ca061ba19aee374c0e2b092bfdef8f9232f2427b9db41e8a8313d7801c44eaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:034d797d41b527133ee4b95d3f453018410ae6ef129f91d426289a7a64951a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385939550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9edd9e299276142eefc649135805ad3cdfa3286411afc9bed5cd4ed2c94b2f94`
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
COPY dir:0423d0cd4a34047821e55a2806cb02fc682f017fba03e4344223878a61041986 in / 
# Wed, 08 Jan 2025 11:00:36 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 08 Jan 2025 11:00:36 GMT
CMD ["/bin/bash"]
# Wed, 08 Jan 2025 11:00:36 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 08 Jan 2025 11:00:36 GMT
LABEL "build-date"="2025-02-13T04:19:45" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
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
	-	`sha256:3333307dcd2e4279579646a05a5f99082a61a20906175240445b0e15f73b6d6e`  
		Last Modified: Thu, 13 Feb 2025 06:13:39 GMT  
		Size: 39.4 MB (39366553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5025173ec0b35686a33458b367c2a6e898c824f57a07925c25d26a0cfb5f2e50`  
		Last Modified: Thu, 13 Feb 2025 06:13:37 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f86fcec3686f77cb176025f6a8eaca71b0dd5350bceb6758b00c852a40f022b`  
		Last Modified: Fri, 14 Feb 2025 03:10:21 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebf1cca43c2d1253e0472cf6518d0b85be73c741e1daaf40baf72dc8fd4f7c1`  
		Last Modified: Fri, 14 Feb 2025 03:10:22 GMT  
		Size: 8.3 MB (8324769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c65a6767f6c3c195b65514ee142c63008c214fd87496a5c088218c962ee0ccc`  
		Last Modified: Fri, 14 Feb 2025 03:10:33 GMT  
		Size: 338.2 MB (338238035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3f9ee31943f5e8a28b7901148df1412e206dd9af97fc2e28e5a4a3bad61edd`  
		Last Modified: Fri, 14 Feb 2025 03:10:21 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bf58cc803fe5de4d75d506220f14da55ce6bc71654b2529b9e52a9d8b36edd`  
		Last Modified: Fri, 14 Feb 2025 03:10:21 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132eb6f17df09da2a17ead4e3834bf4fdb2a661e2f0b9937e1ef836b4c7fb857`  
		Last Modified: Fri, 14 Feb 2025 01:27:41 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8` - unknown; unknown

```console
$ docker pull percona@sha256:7b2112f840c50bdbe34efe8fdc5b57b218d9e8720437cb82f209a7d4ae20f40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 KB (31926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06395a14f1c2523526fda624f09a3fd86fc2793bfb89dd71f25bc9aab7e6eec7`

```dockerfile
```

-	Layers:
	-	`sha256:165ca3e11924692691d164eee96a5c12a417a4bd713186545c049ab7e51b2a40`  
		Last Modified: Fri, 14 Feb 2025 03:10:17 GMT  
		Size: 31.9 KB (31926 bytes)  
		MIME: application/vnd.in-toto+json
