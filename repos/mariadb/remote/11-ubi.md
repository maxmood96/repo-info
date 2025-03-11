## `mariadb:11-ubi`

```console
$ docker pull mariadb@sha256:e854aaf1cfe4e772677cbb0bee870e984f5571b14e1d3c7f602548ddc24c22a0
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
$ docker pull mariadb@sha256:8a50c55a77d36106ca560be55b6e9628f764ef5a877f1b06597a51a459f81cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147415218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d5485f51925c99cbcdf45c4fc683da52268e1d6b73a855dac2542e7f9c972b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL url="https://www.redhat.com"
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL io.openshift.expose-services=""
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 14 Feb 2025 06:55:09 GMT
ENV container oci
# Fri, 14 Feb 2025 06:55:09 GMT
COPY dir:a07d6464b408a07384eb87b8e371fb05260f293df1fdae9e20c1a6653e15e37b in / 
# Fri, 14 Feb 2025 06:55:09 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 06:55:09 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL "build-date"="2025-03-10T09:47:15" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2f8e6c4d7ad22789d5663bf4bd66603301fba889" "build-date"="2025-03-10T09:43:12Z" "release"="1741599792"
# Fri, 14 Feb 2025 06:55:09 GMT
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
	-	`sha256:ecb02bde81105b662eaf8da4b200f811c2ac8a0dd37e0c09f19de54603c5c8fb`  
		Last Modified: Mon, 10 Mar 2025 10:32:31 GMT  
		Size: 39.4 MB (39376539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e92b0a09d78952dd6b3d60aa8a9f9ef1c8282b59a65bcc5aa506acb82686576`  
		Last Modified: Mon, 10 Mar 2025 10:32:31 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86cdc6d6c8721c0336ab4ea62f56ce9e95e4221987321a4dc55e0ead56cab90`  
		Last Modified: Mon, 10 Mar 2025 21:05:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d4a6de3cce60d7ec8aa3f1b3b4720ba018dc9f004d058fe960e140f318d1a0`  
		Last Modified: Mon, 10 Mar 2025 21:05:55 GMT  
		Size: 983.5 KB (983469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65f71ae4f8143eed9d2e1067c9e1e29280b6fd1f362cd448babdc667cd00ec6`  
		Last Modified: Mon, 10 Mar 2025 21:05:55 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a57c2fd7c5dd4157dfb52e8feebc74240f453a12f1703382af42b99d5f3ee5`  
		Last Modified: Mon, 10 Mar 2025 21:05:55 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d760c3870a65426ba245d920fbc35052154f85bd6e406dac58c8cba9463a998a`  
		Last Modified: Mon, 10 Mar 2025 21:05:57 GMT  
		Size: 107.0 MB (107040702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5ab348c8886d5f8a3386026cbb3eb9a09bce92300ec1363136a3f1a01f095d`  
		Last Modified: Mon, 10 Mar 2025 21:05:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021f4c0edecc816ae9d36a30723eb3cd9f8ffbe10856b76b1634bbf9d596a22b`  
		Last Modified: Mon, 10 Mar 2025 21:05:56 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bea40320bbc8ae96d75f2f4e366d9570d97ae680ff6612aff1e031b5cdceee0`  
		Last Modified: Mon, 10 Mar 2025 21:05:56 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:dea0d4791b5fcac80961c6ebcdcec8de184acfb7f3c1fd3d22b63df91004b1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0bdab2033ca528377f921e0d6812d2abe1a48c95151052b6dbb0fbfe4d802b`

```dockerfile
```

-	Layers:
	-	`sha256:0bc03272afc9db53f280dc3dc56799d59589ca185915093a60f61e0b09a10c7f`  
		Last Modified: Mon, 10 Mar 2025 21:05:55 GMT  
		Size: 4.1 MB (4092610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92206b50f78a7a88fda493340315871d4d39e0a65d97975ee821082e12f89f1a`  
		Last Modified: Mon, 10 Mar 2025 21:05:55 GMT  
		Size: 31.6 KB (31553 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:98136fdc19fe62d42175cc3d2dd3a8ba51384cb66f4a21c17a88dfcc76c04f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143836469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20e204c185e948b8f3988ec913132f63523f5c53cc19228fe6b3cd874288762`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL url="https://www.redhat.com"
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL io.openshift.expose-services=""
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 14 Feb 2025 06:55:09 GMT
ENV container oci
# Fri, 14 Feb 2025 06:55:09 GMT
COPY dir:7cf9b7b9f60ce494e82504114b8e4e8497504001337c87ffc50d4a40fe4f9edc in / 
# Fri, 14 Feb 2025 06:55:09 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 06:55:09 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL "build-date"="2025-03-10T09:50:07" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="2f8e6c4d7ad22789d5663bf4bd66603301fba889" "build-date"="2025-03-10T09:43:12Z" "release"="1741599792"
# Fri, 14 Feb 2025 06:55:09 GMT
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
	-	`sha256:f7b8fe7f82e9c2744a37d9d57d915bba00fe3879ae010a254770d6de52407d6b`  
		Last Modified: Mon, 10 Mar 2025 10:36:22 GMT  
		Size: 37.6 MB (37585537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b83df990133b9bdb95a233cede88e14a9e9f42d8a90daca3368a0795857bbf6`  
		Last Modified: Mon, 10 Mar 2025 10:36:20 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df25db65320ff97533159c2664056463735b17d8672ef395850dae4598fbad40`  
		Last Modified: Mon, 10 Mar 2025 21:56:41 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d314a903f0f8ea7ba21dc8471ac60d1d75e14f1212f666509c5fda7d165ab9`  
		Last Modified: Mon, 10 Mar 2025 21:56:42 GMT  
		Size: 913.8 KB (913806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411e4cf428bd410167b4cd0935d9108f6fef4322a4e6afcc67a6cc1d89fc3819`  
		Last Modified: Mon, 10 Mar 2025 21:56:42 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac110afca230a448d3867b0f57a44fd7c654ab2d43f749e94f9dcb3701e580e`  
		Last Modified: Mon, 10 Mar 2025 21:58:38 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da37b57c15659508a0a4e935fafedc6dd5b74dd7cc0ea02e20911d910a521efe`  
		Last Modified: Mon, 10 Mar 2025 21:58:41 GMT  
		Size: 105.3 MB (105322611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb1f7da1f6dfcc6f2ddadbb08dee7615f1e0b3d5e548a2caa55c80b58a9e66c`  
		Last Modified: Mon, 10 Mar 2025 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b33bb7c206ebc4b6da14b75235506f98b01cb85028cf1378d4e8361b24a339`  
		Last Modified: Mon, 10 Mar 2025 21:58:38 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc0fe5fc58a26d0070d2d44fc1d0f0ff6a7714efcd15b00452288e2b554d3e8`  
		Last Modified: Mon, 10 Mar 2025 21:58:39 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:bd2122251f65618796cd9f2c5cd782234daffa646d468046538ff24c17b47687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1412514f018e7590f5efccfebacd5002e415b8b69e05ec7f6db0b371e5558f2b`

```dockerfile
```

-	Layers:
	-	`sha256:711dd84f829b45da9e981af68d1a6eca76047635dae2521cd494670c252e3dcc`  
		Last Modified: Mon, 10 Mar 2025 21:58:38 GMT  
		Size: 4.1 MB (4092475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ad521611ada20e76ecb9a27c5e8e735cfb5ee7974d5b644a58ad3e51969df03`  
		Last Modified: Mon, 10 Mar 2025 21:58:38 GMT  
		Size: 31.7 KB (31721 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2e71e1f87ae67b61b29e29720dfcb271a2177e71484a17d9f565930291dc2aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 MB (157860962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac2633162d94242077257909b1b09da9944109f76f4495dc1ee5239f23cac45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL url="https://www.redhat.com"
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL io.openshift.expose-services=""
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 14 Feb 2025 06:55:09 GMT
ENV container oci
# Fri, 14 Feb 2025 06:55:09 GMT
COPY dir:da1ec7f34262056221a653ac74b71b17804f2abbdaaf0edf8f887dc2c1eeeb91 in / 
# Fri, 14 Feb 2025 06:55:09 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 06:55:09 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL "build-date"="2025-03-10T09:54:50" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="2f8e6c4d7ad22789d5663bf4bd66603301fba889" "build-date"="2025-03-10T09:43:12Z" "release"="1741599792"
# Fri, 14 Feb 2025 06:55:09 GMT
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
	-	`sha256:2ad90c0e47251160a30b1b70efa8a3c13ef0ce7a213f619f4ac82370a7ac2dae`  
		Last Modified: Mon, 10 Mar 2025 12:25:37 GMT  
		Size: 43.8 MB (43784081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4046f47b13f500df13fbbe4b00a43b66c2ff9fcbf6923a82edf7ae12f8ac46d9`  
		Last Modified: Mon, 10 Mar 2025 12:25:36 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515bcae4e6803805c9fb761aa6126102e956ca3841f64368d146a77549e8c806`  
		Last Modified: Mon, 10 Mar 2025 21:15:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be669221bc37a3004a66844eff1b0a2cb4865b5a9c9dc7904113a2051e9f3b7e`  
		Last Modified: Mon, 10 Mar 2025 21:15:59 GMT  
		Size: 904.3 KB (904313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f1977acf3cc2f8a13341dd25005b8da9300fb2c777fd84a0758d013101353`  
		Last Modified: Mon, 10 Mar 2025 21:15:59 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c8ccaf986036b54c5f1554a5ce79ab38cb22432b74a05f4f0f979390e1c2dd`  
		Last Modified: Mon, 10 Mar 2025 21:47:49 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d34cd01b0d7856ab358eea6b7aee7080190efba611fba2f6800cfe159590ea8`  
		Last Modified: Mon, 10 Mar 2025 21:47:53 GMT  
		Size: 113.2 MB (113158047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a872deadc8a1a9fbe9358b9370b4b3751795735f94e9f795016d8cf211d65dc`  
		Last Modified: Mon, 10 Mar 2025 21:47:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf39e880b5e7dfe974d573faf61a42b08219325317330fdff4394b907d21484`  
		Last Modified: Mon, 10 Mar 2025 21:47:49 GMT  
		Size: 4.0 KB (4040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ba410ad4863087e1c6ba9928ec7ddc4cf1113586c96e660e4f45587f12f234`  
		Last Modified: Mon, 10 Mar 2025 21:47:50 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:2c87a1e6107fda00fde9a90cac1a0379ebf9179c8f66fdb7f2138586cac750d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2eaf65d195da528b1bf2962aaf560166e1c84109d50fa0706d96828bc1a6186`

```dockerfile
```

-	Layers:
	-	`sha256:6cacae7bfa200b2a1bb72d432f85feec8d167a62dd8bda3273e7f25d1f1652a7`  
		Last Modified: Mon, 10 Mar 2025 21:47:50 GMT  
		Size: 4.1 MB (4093678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fe146827c0f0cb2c7403be4b6f58567392ef9c5d18525f665e01db614f98015`  
		Last Modified: Mon, 10 Mar 2025 21:47:49 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:2d65afa37c4d53fc36f5932130d039ea81a86b7b75842d5f3953f1e4f892e547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146095141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069b1426b8070f04e5c0fe78b2dba9e7a0f67d955bc1437f07ce990a9bd7a0a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL url="https://www.redhat.com"
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL io.openshift.expose-services=""
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 14 Feb 2025 06:55:09 GMT
ENV container oci
# Fri, 14 Feb 2025 06:55:09 GMT
COPY dir:03a99625d811dfe52ab91eb1e2d9bde6f2635b5ecea85281c88b7104fd8fc9f2 in / 
# Fri, 14 Feb 2025 06:55:09 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 06:55:09 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL "build-date"="2025-03-10T09:50:03" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="2f8e6c4d7ad22789d5663bf4bd66603301fba889" "build-date"="2025-03-10T09:43:12Z" "release"="1741599792"
# Fri, 14 Feb 2025 06:55:09 GMT
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
	-	`sha256:9f806440d1e665fa608505f763022c8e47b2f9e29ccfb38f0816ce15a450c4b9`  
		Last Modified: Mon, 10 Mar 2025 12:25:32 GMT  
		Size: 37.5 MB (37537281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf806b0d10a5106a3d4d54aa3f736209953daa8a47543d90b3c7592b486b3a9d`  
		Last Modified: Mon, 10 Mar 2025 12:25:31 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da44457f66f1c09c06ab05b312bce450839bd8b48db1e7442de4fc49e922336d`  
		Last Modified: Mon, 10 Mar 2025 21:15:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1571db08c6265a23abde3155942064c7f42a63a9a8a34c0e9170f1a9a8fc95a9`  
		Last Modified: Mon, 10 Mar 2025 21:15:11 GMT  
		Size: 948.1 KB (948114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8958ea09e9bda1232c702751b3c24e38602c7732013430c4772826d76862c6f8`  
		Last Modified: Mon, 10 Mar 2025 21:18:53 GMT  
		Size: 299.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53137757d14da1142cf69ed2fce35bdd94f8ad6cf3b6a074fe9701c3bdc303e9`  
		Last Modified: Mon, 10 Mar 2025 21:18:53 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973f91c57177255f2f69172e345d9898be884e16a2ebfc3935d898ffb1f2829d`  
		Last Modified: Mon, 10 Mar 2025 21:18:55 GMT  
		Size: 107.6 MB (107595237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222fb8e1fe6d909d15e544c4a8606fde920d79beb36c5855794fb77a0a72bd51`  
		Last Modified: Mon, 10 Mar 2025 21:18:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1889dad75d9b2841cac3f06b9a5bed954dc560bdf610d2257410775b7332c051`  
		Last Modified: Mon, 10 Mar 2025 21:18:54 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27821d799fed0bbb715c4716e11a9de279e51aaaab3f81fa87dad86786a0a8d`  
		Last Modified: Mon, 10 Mar 2025 21:18:54 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:1ec4c572264583d68d508e9cd5f81a88b58a07fcb0ef86a3d5986689c8d2c6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b153defa24a98f460488a540b4e4d129340150ce86dae7833b1d0c01991ec8`

```dockerfile
```

-	Layers:
	-	`sha256:df98a135036f4d9df8c54a55fde4bd0abf2cfe04e7512e5b2c2fde0b730600ec`  
		Last Modified: Mon, 10 Mar 2025 21:18:53 GMT  
		Size: 4.1 MB (4093663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da3473ae1d1af67806a575e927a814259e8fca098ceca67fef7d840a2f033fa`  
		Last Modified: Mon, 10 Mar 2025 21:18:53 GMT  
		Size: 31.6 KB (31554 bytes)  
		MIME: application/vnd.in-toto+json
