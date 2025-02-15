## `mariadb:11-ubi`

```console
$ docker pull mariadb@sha256:f6dfba8f3e27462912a6235dc745aa926e5d3e00b9e95579affec299c42a5b20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `mariadb:11-ubi` - linux; amd64

```console
$ docker pull mariadb@sha256:b97aa084f2be984e9ab6633c7c7c64b804d285abebe3d8f446f812a2eddc00a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147403983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4896688841994633f3bfac5fd486e910c8c01cea4f211242825f0377b6de2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL url="https://www.redhat.com"
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL io.openshift.expose-services=""
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 13 Feb 2025 04:20:08 GMT
ENV container oci
# Thu, 13 Feb 2025 04:20:08 GMT
COPY dir:0423d0cd4a34047821e55a2806cb02fc682f017fba03e4344223878a61041986 in / 
# Thu, 13 Feb 2025 04:20:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 13 Feb 2025 04:20:08 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 04:20:08 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 13 Feb 2025 04:20:08 GMT
LABEL "build-date"="2025-02-13T04:19:45" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
# Thu, 13 Feb 2025 04:20:12 GMT
RUN /bin/sh
# Fri, 14 Feb 2025 06:55:09 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV GOSU_VERSION=1.17
# Fri, 14 Feb 2025 06:55:09 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.7.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.7.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Feb 2025 06:55:09 GMT
ARG MARIADB_VERSION=11.7.2
# Fri, 14 Feb 2025 06:55:09 GMT
ENV MARIADB_VERSION=11.7.2
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: MARIADB_VERSION=11.7.2
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: MARIADB_VERSION=11.7.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Feb 2025 06:55:09 GMT
USER mysql
# Fri, 14 Feb 2025 06:55:09 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["mariadbd"]
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
	-	`sha256:98a6dbb6d0230bfa8427411dc7f445f98780b82651eb963d1199456ae9f4d57b`  
		Last Modified: Sat, 15 Feb 2025 01:36:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac042c48e435a4281e08e4b28afaad8e34f0726a4fc3d6c1e8d98a58e71fe8f6`  
		Last Modified: Sat, 15 Feb 2025 01:36:55 GMT  
		Size: 983.5 KB (983461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bfd1dd0ddf8daaf2ae5f93257886f43fc8847604b50f24a4c67816ba2b850a`  
		Last Modified: Fri, 14 Feb 2025 22:47:55 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a1fd3436d9eeeb58287612a7162580991ad991a2248ea0e10a628d9e842943`  
		Last Modified: Fri, 14 Feb 2025 22:47:57 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d46a123f5ed3cf89de0a50e80534c68bd88e8e92bc47ea6a3b05e9318e7bda`  
		Last Modified: Sat, 15 Feb 2025 01:36:59 GMT  
		Size: 107.0 MB (107039460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fae9e47d8da0838d138a46c04abd6cd825e4b4ebb151db24968ea40a13344b`  
		Last Modified: Sat, 15 Feb 2025 01:36:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7147a35bf06edf04cb9143e0327a0bce04de798b8d079bdc63ae21f6a2c43`  
		Last Modified: Fri, 14 Feb 2025 22:48:03 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ec5ef088158734f7542b7936d1608943b996d52f749288300581a9d0396031`  
		Last Modified: Fri, 14 Feb 2025 22:48:08 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:bd0fc0ed3979f048ac40ea066810555bfed1b5a75a23cb8e61897865a3d9297e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb0f966379a9cd078021838580434f4404c6a8494108c01fd6068d5773383296`

```dockerfile
```

-	Layers:
	-	`sha256:dc3e6eef6166029495d66091c5336a1c18003bfa84c0fff6b570383b1b0a6ad8`  
		Last Modified: Sat, 15 Feb 2025 01:35:45 GMT  
		Size: 4.1 MB (4092610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e47f2a362b3ba49cdc09620bd4676cf28cf5b77a6a6b9aa274dc3d0509abe475`  
		Last Modified: Sat, 15 Feb 2025 01:35:45 GMT  
		Size: 31.6 KB (31554 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:df11c30b0f9136888680f1349e6d634d6aef4c9799249359cca1a6d33246cbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143153791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22aa240d29ec8ee34f2544458b1d22d245054826084b5d0fc2b2c3b1e2be8c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL url="https://www.redhat.com"
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 21 Nov 2024 21:43:46 GMT
ENV container oci
# Thu, 21 Nov 2024 21:43:46 GMT
COPY dir:5809c16e2c5c048de6a8d8eea9437ac183b7d2503e26b24a2422ead5736aecad in / 
# Thu, 21 Nov 2024 21:43:46 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 21 Nov 2024 21:43:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Nov 2024 21:43:46 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL "build-date"="2025-02-13T04:25:01" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
# Thu, 21 Nov 2024 21:43:46 GMT
RUN /bin/sh
# Thu, 21 Nov 2024 21:43:46 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 21:43:46 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.6.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.6.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 21 Nov 2024 21:43:46 GMT
ARG MARIADB_VERSION=11.6.2
# Thu, 21 Nov 2024 21:43:46 GMT
ENV MARIADB_VERSION=11.6.2
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: MARIADB_VERSION=11.6.2
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: MARIADB_VERSION=11.6.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 21:43:46 GMT
USER mysql
# Thu, 21 Nov 2024 21:43:46 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 21 Nov 2024 21:43:46 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:56631da24b0de345717238daea2e3e61c768d081572916ae06b08b19126a740d`  
		Last Modified: Thu, 13 Feb 2025 06:13:39 GMT  
		Size: 37.6 MB (37626059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aee836c3728069e82153bf7b209c409d3343adaea6ab6b31546e5ce09250db5`  
		Last Modified: Thu, 13 Feb 2025 06:13:36 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96e7e286423268016ac62960168898b48e766de6d61572e4d02525dc914a24b`  
		Last Modified: Fri, 14 Feb 2025 01:37:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ecd0242962bdf3a81d71edbe6166616f5aca0d3fe0f117e499900c8c1f95f`  
		Last Modified: Fri, 14 Feb 2025 01:37:47 GMT  
		Size: 913.8 KB (913805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bb7288c33b544b8a03ba07c4af824b547c0437c1f32254d35b08cb1e3a3513`  
		Last Modified: Fri, 14 Feb 2025 01:44:56 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c427242c814991ae9a03f7f88bf42eeb2a5eb11bff47806ac0f5dde619b532ae`  
		Last Modified: Fri, 14 Feb 2025 01:44:56 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563dfeefa9a180f77ec7709570c5ebc6124f67a4d846660f6d174b5552302d77`  
		Last Modified: Fri, 14 Feb 2025 01:45:09 GMT  
		Size: 104.6 MB (104599416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcff33aca47067a019c819ed94223f8f6478296e5b19737bf21fd9608379a03f`  
		Last Modified: Fri, 14 Feb 2025 01:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75c99ab4a425d7750ff492ea69998559219a3dfcd73a53b4fe8db838ac82550`  
		Last Modified: Fri, 14 Feb 2025 01:44:57 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c591cb26eb8a08eff6f3f15d1588f30d4d6ac3d72c99b77fdab06dad7078e6`  
		Last Modified: Fri, 14 Feb 2025 01:44:58 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:e2506ec594cfb9d1a9e08fd44356fded5a0ed5043df20a9a7997a56beb63dad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4056800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a642f6065c8565dbb1a39143bc16fc4565f370a6cdcf1ed8398002aff1f4e1f2`

```dockerfile
```

-	Layers:
	-	`sha256:2fb22f04728b076d04426da97f2e62a880b3eaac73fc21f1396a6d6aaf29a6c5`  
		Last Modified: Fri, 14 Feb 2025 01:36:12 GMT  
		Size: 4.0 MB (4025116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b4260e41a6c704cca7a71530fd64364e20eace2b58ab4696f0bf304df79ccd`  
		Last Modified: Fri, 14 Feb 2025 01:36:12 GMT  
		Size: 31.7 KB (31684 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cfb7bf1a11b4cb6fd0769807b74267b0c74afec594e2189471bf444913cc76e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157049550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5615bf06a8b8a1b5d0811b6697e371613046f229c1f6b0ade79a4fcea0c1059d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL url="https://www.redhat.com"
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 21 Nov 2024 21:43:46 GMT
ENV container oci
# Thu, 21 Nov 2024 21:43:46 GMT
COPY dir:2c0c7900d5f6c40d02b1787c7aed15027e6a404d210587076552b87add6a3c87 in / 
# Thu, 21 Nov 2024 21:43:46 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 21 Nov 2024 21:43:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Nov 2024 21:43:46 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL "build-date"="2025-02-13T04:27:14" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
# Thu, 21 Nov 2024 21:43:46 GMT
RUN /bin/sh
# Thu, 21 Nov 2024 21:43:46 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 21:43:46 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.6.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.6.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 21 Nov 2024 21:43:46 GMT
ARG MARIADB_VERSION=11.6.2
# Thu, 21 Nov 2024 21:43:46 GMT
ENV MARIADB_VERSION=11.6.2
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: MARIADB_VERSION=11.6.2
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: MARIADB_VERSION=11.6.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 21:43:46 GMT
USER mysql
# Thu, 21 Nov 2024 21:43:46 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 21 Nov 2024 21:43:46 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9e6b2a031935c86976201f383962f66d759b1c458d46f7f8db9cd32663dd945f`  
		Last Modified: Thu, 13 Feb 2025 06:13:41 GMT  
		Size: 43.8 MB (43777674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65b64183df0b784e7e5f8c0c986254fe70af80954963d80c5fa6ab3c2e153af`  
		Last Modified: Thu, 13 Feb 2025 06:13:37 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07d4603927a3711a16ca37d2f56fcab04e80bb63fb45f886aab0e90c67c1316`  
		Last Modified: Fri, 14 Feb 2025 02:06:39 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870c16dcd714cae1813543650d7caabc47cd589ea1e8450ff7397e21533e50ea`  
		Last Modified: Fri, 14 Feb 2025 02:06:41 GMT  
		Size: 904.3 KB (904302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ab6e905a7da7466738b39b73e94f0ba3bb583443a159cc18075ad25f1afe78`  
		Last Modified: Fri, 14 Feb 2025 02:08:51 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86278c85861d10112eee7b69bfbb115a883d742afba522a26b0c1d67ac067fc3`  
		Last Modified: Fri, 14 Feb 2025 02:08:52 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ae4e29c602acc9bc7bcf5a80aa64f4f74163dc6f73b0b7c81f691cc1e924f2`  
		Last Modified: Fri, 14 Feb 2025 02:08:51 GMT  
		Size: 112.4 MB (112353061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a100effb50b4fec186ec704ffcd5f27faa5b785f01cfc062a53a7dc3a7e21b8d`  
		Last Modified: Fri, 14 Feb 2025 02:08:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd741355a093785ca996d823f4baaf326beb84a4d61b37c297294a15dd9cebe`  
		Last Modified: Fri, 14 Feb 2025 02:08:39 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d0b1d0b1f4318d821d9376f930a5924fe53bb09e518a3edc2a9a6691233ee0`  
		Last Modified: Fri, 14 Feb 2025 02:08:37 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:f15efdd1bd6a580e1cc3f178be5cea046e308936bf28660f916a1395df3a5b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148ecfc44f40215d60fac2a9146a7909ed74b53aab07b9fd4f0727e69ccc7f29`

```dockerfile
```

-	Layers:
	-	`sha256:c57fc937a828e25ccec9f99a31ac6642a05f81ab12ac9b6cbcecaf2041342234`  
		Last Modified: Fri, 14 Feb 2025 01:36:14 GMT  
		Size: 4.0 MB (4026319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f3333ebd05702bd865cc02c692b5e4d45fd346b075efd319aa6e6cdd750d29`  
		Last Modified: Fri, 14 Feb 2025 01:36:14 GMT  
		Size: 31.6 KB (31574 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:f91bddb1dd72190812be971ded08f5b6f1823de86abac50672c0f5b3fd3c05c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145391819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d125dcd275d78fa98d450e1de50943e09b3f0c5befd5608bfcb4c8105a4570`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL url="https://www.redhat.com"
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 21 Nov 2024 21:43:46 GMT
ENV container oci
# Thu, 21 Nov 2024 21:43:46 GMT
COPY dir:c862cae3542fa73c4d0881791f411d054c541dacc4430391519579fe17851861 in / 
# Thu, 21 Nov 2024 21:43:46 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 21 Nov 2024 21:43:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Nov 2024 21:43:46 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL "build-date"="2025-02-13T04:22:40" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
# Thu, 21 Nov 2024 21:43:46 GMT
RUN /bin/sh
# Thu, 21 Nov 2024 21:43:46 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 21:43:46 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.6.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 21 Nov 2024 21:43:46 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.6.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 21 Nov 2024 21:43:46 GMT
ARG MARIADB_VERSION=11.6.2
# Thu, 21 Nov 2024 21:43:46 GMT
ENV MARIADB_VERSION=11.6.2
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: MARIADB_VERSION=11.6.2
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
VOLUME [/var/lib/mysql]
# Thu, 21 Nov 2024 21:43:46 GMT
# ARGS: MARIADB_VERSION=11.6.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 21:43:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 21:43:46 GMT
USER mysql
# Thu, 21 Nov 2024 21:43:46 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 21 Nov 2024 21:43:46 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:2a473e1a3c46f4f695fac29b3f07299216de74886d72d8a6ee099c88e522d425`  
		Last Modified: Thu, 13 Feb 2025 06:13:39 GMT  
		Size: 37.6 MB (37555898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b2c3df35599710f44a071f13be3fc08bdd10402bdd2d9cf10dfee0af30c3e6`  
		Last Modified: Thu, 13 Feb 2025 06:13:37 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e296bf87bfc317d13d9efa1cf45bc7b2ddb6d1da0a0759710c7aab3f724abd18`  
		Last Modified: Fri, 14 Feb 2025 11:05:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9544b4e662bc943ab5dda959ab1ec82b3b19f35447c2c1541c54ffd2a91a6723`  
		Last Modified: Fri, 14 Feb 2025 11:06:03 GMT  
		Size: 948.1 KB (948116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dacb864b99c4533bbb7c7ce4c89cf4749938e7fdd32ba357babf75ebd43cce1`  
		Last Modified: Fri, 14 Feb 2025 11:06:09 GMT  
		Size: 299.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d7abd67b6eb817c7f5d801a6d437a3c917b55bde1c8c5007f3178d63a7642f`  
		Last Modified: Fri, 14 Feb 2025 11:06:14 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c37556d205f1ab0daeb846c08ddcdd33095e4b349712f5655136cfcca6efb3a`  
		Last Modified: Fri, 14 Feb 2025 07:10:44 GMT  
		Size: 106.9 MB (106873289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac90eac16cf9dcd48b3702c409279779c941c82123afbaafdd1994e1dff9de`  
		Last Modified: Fri, 14 Feb 2025 11:08:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f596b22c0de9f139d5d33685569cbcc4969a6e979f0f6ad91ee81dfdcf9bed6`  
		Last Modified: Fri, 14 Feb 2025 11:08:10 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2d879bce52959e1cb2d6643527a5ad458f35e56bfdf0cfc18347b546ce282d`  
		Last Modified: Fri, 14 Feb 2025 11:08:14 GMT  
		Size: 8.4 KB (8402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:9ff03c5a7531c824f0534c61117357156b67fb9539856ca940f6c9716b391e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70465bfff3e8b212796691499686d6f4dccb8d85d709132dce360fa4444f8c3c`

```dockerfile
```

-	Layers:
	-	`sha256:bf53033e0e0562cf54fba6e98e179b73960f8e1733a17d54b13d4c0423cf35de`  
		Last Modified: Fri, 14 Feb 2025 10:35:58 GMT  
		Size: 4.0 MB (4026304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3666e465e30666fc9b6b6457ef7274951590c095cbf917dca4addbe6822a15fb`  
		Last Modified: Fri, 14 Feb 2025 10:35:58 GMT  
		Size: 31.5 KB (31518 bytes)  
		MIME: application/vnd.in-toto+json
