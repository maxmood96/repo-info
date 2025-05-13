## `percona:ps-8.0.41-32`

```console
$ docker pull percona@sha256:d1bb8baa13f043a8497e52405f42a8221c1719c7a6df951e0e68231d32e09792
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0.41-32` - linux; amd64

```console
$ docker pull percona@sha256:bf0741e8f46d21ce76042462c947f0a4ff46fa376cff83d694802c918cb0a840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363290324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332b60e703286b2d26d45375e53b1c4552eb105d45ae45f38f0a2fbc04fbf121`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL url="https://www.redhat.com"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.expose-services=""
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 18 Feb 2025 16:18:37 GMT
ENV container oci
# Tue, 18 Feb 2025 16:18:37 GMT
COPY dir:2dc25289c3b10f6fae681d085452474bf4d133d8f435510e0e9aa64114b861ab in / 
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 16:18:37 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 18 Feb 2025 16:18:37 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL "build-date"="2025-05-13T04:42:10" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7575d7eb45eb7f545fef31ba067dfe3d8e52c4eb" "release"="1747111267"
# Tue, 18 Feb 2025 16:18:37 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 18 Feb 2025 16:18:37 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_VERSION=8.0.41-32.1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV OS_VER=el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_PERCONA_VERSION=8.0.41-32.1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_REPO=testing
# Tue, 18 Feb 2025 16:18:37 GMT
ENV PS_TELEMETRY_VERSION=8.0.41-32-1
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 18 Feb 2025 16:18:37 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 18 Feb 2025 16:18:37 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 18 Feb 2025 16:18:37 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 18 Feb 2025 16:18:37 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 18 Feb 2025 16:18:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Feb 2025 16:18:37 GMT
USER mysql
# Tue, 18 Feb 2025 16:18:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Feb 2025 16:18:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:719fed365262e942a8d13a9f7c6f9e87e6274c4e3ad3d0efc81666b12229084d`  
		Last Modified: Tue, 13 May 2025 05:25:18 GMT  
		Size: 39.7 MB (39714170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c0a8660fa8b45240c89291d79addb321002cbc67d7e64da3dafc4a5d29ca19`  
		Last Modified: Tue, 13 May 2025 19:55:13 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4929fb32d5da2dffc6ed6de37f64c84b2ed1da99cbb430f01c5a7ede71ee3ab5`  
		Last Modified: Tue, 13 May 2025 19:55:14 GMT  
		Size: 8.8 MB (8842269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22960db0acf5feec4833c7d1a5670dd30bddc5af53ef33ad39f5a8b2a68acc2`  
		Last Modified: Tue, 13 May 2025 19:55:20 GMT  
		Size: 314.7 MB (314724150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e336521adc5c8bcd7656a0c4f5175b017b13d3790972ab475d080bcace9e7e62`  
		Last Modified: Tue, 13 May 2025 19:55:13 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb56355e9d9d77a12a7812d5311fe1b53c251837151d2d087c2bc04132b38815`  
		Last Modified: Tue, 13 May 2025 19:55:14 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169596d6f0e84f2aae03f537ede3809acaf6fa386faeae8421f53aa9fdd30be`  
		Last Modified: Tue, 13 May 2025 19:55:15 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0.41-32` - unknown; unknown

```console
$ docker pull percona@sha256:502e0278697947ebcd878b77275639d9273be00cf7b23ba21d451fcf0ed69a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dcba09f6688579aab1bb06b86ecbdd5a8411e6cfd9d3eedd4261c01c311d0e`

```dockerfile
```

-	Layers:
	-	`sha256:e3547e54646f1b7b071de9ca50869b71c4171d34089d1e3a9f5470cbf1dbd52d`  
		Last Modified: Tue, 13 May 2025 19:55:13 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json
