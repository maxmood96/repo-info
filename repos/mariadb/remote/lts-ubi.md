## `mariadb:lts-ubi`

```console
$ docker pull mariadb@sha256:c9d91ef1a460d872dc7cae07c5eeb7f1ca340cba8dbc2bdf0fa657ffc70094d1
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

### `mariadb:lts-ubi` - linux; amd64

```console
$ docker pull mariadb@sha256:1154ac7ea3818d8c6291215397fcf2ac519188a717f068b0c0fc6f85bcbbb1e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147609761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72febda7c18024f76cda233448032f9ca681577e98b183e5a7c10435f3bce238`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL url="https://www.redhat.com"
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 10 Jun 2025 21:48:21 GMT
ENV container oci
# Tue, 10 Jun 2025 21:48:21 GMT
COPY dir:9f1e3d7980aa1b8b007cf8dcf05575fff696655332be09ae87c8f7de7f00e923 in / 
# Tue, 10 Jun 2025 21:48:21 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 21:48:21 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL "build-date"="2025-06-24T16:31:57" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Tue, 10 Jun 2025 21:48:21 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENV GOSU_VERSION=1.17
# Tue, 10 Jun 2025 21:48:21 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 10 Jun 2025 21:48:21 GMT
ARG MARIADB_VERSION=11.8.2
# Tue, 10 Jun 2025 21:48:21 GMT
ENV MARIADB_VERSION=11.8.2
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: MARIADB_VERSION=11.8.2
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
VOLUME [/var/lib/mysql]
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: MARIADB_VERSION=11.8.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Jun 2025 21:48:21 GMT
USER mysql
# Tue, 10 Jun 2025 21:48:21 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7073092d8bcd7b6d72345cfa87d8389a33f629b3c49ff887ad3a51c6ed8dfd83`  
		Last Modified: Tue, 24 Jun 2025 18:09:29 GMT  
		Size: 39.7 MB (39650665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cc161ae222da6b32c5d9570f6e74c8644458a56e5a53e1c3d7dc9c97dc37e8`  
		Last Modified: Wed, 25 Jun 2025 17:54:37 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ec6edd9ccae5eb5ec78bbea4d1195345f182e03acc1d2482a009803c525207`  
		Last Modified: Wed, 25 Jun 2025 18:08:59 GMT  
		Size: 983.5 KB (983468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906078e4b43e20a99bf84f5892e8ff703c956fdae28b20242b7554c7f4ab753f`  
		Last Modified: Wed, 25 Jun 2025 18:09:05 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe4cd903319439085670755b8d85b3a2f864d02ac4154266504342f190aa1e7`  
		Last Modified: Wed, 25 Jun 2025 18:09:08 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbf3423ec71d6b2e7d9e2b3600f292ea3d08cc09e9ed06f6731446f425c5450`  
		Last Modified: Wed, 25 Jun 2025 18:36:58 GMT  
		Size: 107.0 MB (106961574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea752017fdcaf808be8865649b23b7bb5e6fad7d7fd3b2413d6539230efeb832`  
		Last Modified: Wed, 25 Jun 2025 18:09:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf738db70cb50359ed51d02a9a1dff23ba1d086c348569f64884d5ed7bd7823`  
		Last Modified: Wed, 25 Jun 2025 18:09:15 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c5294365e413e3e3a4daeb9f8c3ec7d0303d424383dafef0f37aafa5372b83`  
		Last Modified: Wed, 25 Jun 2025 18:09:17 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:5c8d4104267a6c8d404cd175c1ce7da0b3af155986c4237c332ac50bab9450d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40f8484cd098ce4b264a43716342bceb1a0949740b9c65d423aebcee10c0ba4`

```dockerfile
```

-	Layers:
	-	`sha256:7a2a85c2d20546afb155437abcdbd48fddf7d37eac5a225fb1712f1cd2364777`  
		Last Modified: Wed, 25 Jun 2025 18:35:53 GMT  
		Size: 4.1 MB (4139612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc16c928cdf04f5258aa2083ffc7a68749d52d230789b18602dc0ed780f7015`  
		Last Modified: Wed, 25 Jun 2025 18:35:54 GMT  
		Size: 30.8 KB (30772 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f081c9d2297e88a1a31239f7b3f13f0b611cd0782336bd4da51a9cad8b1c272a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144218541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4743f8d68e0105e85870c88ef62b4428bb7374d62ca53fc478e4dfd0322500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL url="https://www.redhat.com"
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 10 Jun 2025 21:48:21 GMT
ENV container oci
# Tue, 10 Jun 2025 21:48:21 GMT
COPY dir:837c51d2245269e7540005032254a14f4d0618334b5c45ecacf5b0c7968d0657 in / 
# Tue, 10 Jun 2025 21:48:21 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 21:48:21 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL "build-date"="2025-06-24T16:36:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Tue, 10 Jun 2025 21:48:21 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENV GOSU_VERSION=1.17
# Tue, 10 Jun 2025 21:48:21 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 10 Jun 2025 21:48:21 GMT
ARG MARIADB_VERSION=11.8.2
# Tue, 10 Jun 2025 21:48:21 GMT
ENV MARIADB_VERSION=11.8.2
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: MARIADB_VERSION=11.8.2
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
VOLUME [/var/lib/mysql]
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: MARIADB_VERSION=11.8.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Jun 2025 21:48:21 GMT
USER mysql
# Tue, 10 Jun 2025 21:48:21 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:ba92c2079b2b21a2f178ace5ca98b5ef2d5cd02901c30e48729b7afe34ecd27e`  
		Last Modified: Tue, 24 Jun 2025 18:09:22 GMT  
		Size: 37.9 MB (37864307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b795dd2bc8a088599b0b3058e11bc11694cc82ac10b13302b61db785b9c7568`  
		Last Modified: Wed, 25 Jun 2025 23:12:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554425bb2654eb76443e007d5975b0b9db73b5f9a98dfd6c06a5fba28da0046f`  
		Last Modified: Wed, 25 Jun 2025 23:12:34 GMT  
		Size: 913.8 KB (913808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f166e88b135172f40515b2214fac9d5e09c03a2b19f8cd4d7b84d2e99591fe46`  
		Last Modified: Wed, 25 Jun 2025 23:12:34 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a5756307348244e68d6f73ef427ccf840e1b9a9871b3b961bc96f6875246a4`  
		Last Modified: Wed, 25 Jun 2025 23:13:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1feb8b3ef6e5c9fed87495cd2193a699b3e49c8150b9e89da2dcdd95dc23ae`  
		Last Modified: Wed, 25 Jun 2025 23:13:56 GMT  
		Size: 105.4 MB (105426370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c123c91afd95ff6e86cde576b4e5ca6533ac4eeb5ae1f6d2bf90d6d222c555`  
		Last Modified: Wed, 25 Jun 2025 23:13:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893d0c96de257609a92966dfef6a3bc37a4e1bbbaa2636746ea979ffa7792b1d`  
		Last Modified: Wed, 25 Jun 2025 23:13:48 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434ce950e41e995e799d50c298097cd21581b6041e8ec51281fde98af70a00f2`  
		Last Modified: Wed, 25 Jun 2025 23:13:48 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:db94e21a225781f7a5f0f617b079900fa04afe03a52071e910272248a13506e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe66a0fda07f8ddf0e004286203899f4666cd521f29b63ff41b630e8d7754d82`

```dockerfile
```

-	Layers:
	-	`sha256:c5af7591ee9f6f2e9cde664085a1dd47f0c601e49ee09299dd9e2d048124cec4`  
		Last Modified: Thu, 26 Jun 2025 00:35:55 GMT  
		Size: 4.1 MB (4139678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b87f2bb2b4221efc9027f87ecc3e0d53f94f316fb62443e1505ddb09af3a5c04`  
		Last Modified: Thu, 26 Jun 2025 00:35:56 GMT  
		Size: 31.0 KB (30965 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:001607ae2e4bbc1e57d3e317ee3f64c1e2727d0e093f8fc75b13bdcbc810b59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158257117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52005e80bd13090d0da6e6fdd0e78cf367f682339309d8d7feda385b9a031c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL url="https://www.redhat.com"
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 10 Jun 2025 21:48:21 GMT
ENV container oci
# Tue, 10 Jun 2025 21:48:21 GMT
COPY dir:d83abf82dbf4be7abfad8c73a5c54416daede00b99a88ceef5492299e80e8120 in / 
# Tue, 10 Jun 2025 21:48:21 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 21:48:21 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL "build-date"="2025-06-24T16:34:39" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Tue, 10 Jun 2025 21:48:21 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENV GOSU_VERSION=1.17
# Tue, 10 Jun 2025 21:48:21 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 10 Jun 2025 21:48:21 GMT
ARG MARIADB_VERSION=11.8.2
# Tue, 10 Jun 2025 21:48:21 GMT
ENV MARIADB_VERSION=11.8.2
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: MARIADB_VERSION=11.8.2
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
VOLUME [/var/lib/mysql]
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: MARIADB_VERSION=11.8.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Jun 2025 21:48:21 GMT
USER mysql
# Tue, 10 Jun 2025 21:48:21 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8374cdcea99a5f341eb5030b5ece88085798cef7a6357cfcc46f8db2ab3dcbc9`  
		Last Modified: Tue, 24 Jun 2025 18:09:28 GMT  
		Size: 44.0 MB (44041398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5a972b3f6e76896738e710ac45e18fe2517253e3673e1496ade518688040b0`  
		Last Modified: Wed, 25 Jun 2025 18:14:39 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e7a41c1ecdc38959634d42d071eae6783d74fe336f945cae88cc7d6340e23c`  
		Last Modified: Wed, 25 Jun 2025 18:14:43 GMT  
		Size: 904.3 KB (904312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2122c787cb97ed3f696f683dbe6f4fe025d601c748225653e2fb949d18eed0`  
		Last Modified: Wed, 25 Jun 2025 18:16:06 GMT  
		Size: 300.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea038ab38c045d2eafe6e626237042c3162f8fabea2a43a59c50d90566f9814`  
		Last Modified: Wed, 25 Jun 2025 18:16:10 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf25190164ef427a7a34c85e862bde0a33390fe6a6e5964df2cd7856b7f1d38`  
		Last Modified: Thu, 26 Jun 2025 01:03:45 GMT  
		Size: 113.3 MB (113297354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc73020206b8305e42cb564b9b65a05f65ad0d20cd5b6cd374cfa6aa9af35d4`  
		Last Modified: Wed, 25 Jun 2025 18:16:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3570c3232c7e4a8cd79082312fadd76e5f895a58e544087e0a042a8e233b92e`  
		Last Modified: Wed, 25 Jun 2025 18:16:16 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91222396f78c671e3bc02fa5162df15d33af054cc6d762d3004255641014e7fa`  
		Last Modified: Wed, 25 Jun 2025 18:16:20 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:586ae9cc8193284514cf1fa3e23da226d6d86270f4f46c95cbc19f825db686c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a404fb1a4997cd76f06454cb2ac7a961058f13ea1c93b2c8af3d925cda2c250b`

```dockerfile
```

-	Layers:
	-	`sha256:9aa15a9ab7eaee7161b975310c1bf6e7840b0e900084d3acc10b90bd947a4d94`  
		Last Modified: Wed, 25 Jun 2025 21:36:07 GMT  
		Size: 4.1 MB (4140869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e6259bb1d6f1702e8ab5c69bcedbb7461f4e94cdf5449d493e48280325474a7`  
		Last Modified: Wed, 25 Jun 2025 21:36:08 GMT  
		Size: 30.8 KB (30842 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:2eaae47e0f4e5e899405c7bdefa99382030d885450702f3202c5b0db900c77ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146413165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085d2bccc4095cc54ac908d8f8b5c978fc9487db31947da8652c89dde0f51c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL url="https://www.redhat.com"
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 10 Jun 2025 21:48:21 GMT
ENV container oci
# Tue, 10 Jun 2025 21:48:21 GMT
COPY dir:e2a83cbb368dbfe11a6a9aa86493d965978673a0761d29b05526a8733ebbd9fe in / 
# Tue, 10 Jun 2025 21:48:21 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 21:48:21 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL "build-date"="2025-06-24T16:41:50" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Tue, 10 Jun 2025 21:48:21 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENV GOSU_VERSION=1.17
# Tue, 10 Jun 2025 21:48:21 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 10 Jun 2025 21:48:21 GMT
ARG MARIADB_VERSION=11.8.2
# Tue, 10 Jun 2025 21:48:21 GMT
ENV MARIADB_VERSION=11.8.2
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: MARIADB_VERSION=11.8.2
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
VOLUME [/var/lib/mysql]
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: MARIADB_VERSION=11.8.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Jun 2025 21:48:21 GMT
USER mysql
# Tue, 10 Jun 2025 21:48:21 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f5839fc3095af9677cbac70df8d81adaddb0cf690ee35af534232f47f1449bd8`  
		Last Modified: Tue, 24 Jun 2025 18:09:23 GMT  
		Size: 37.8 MB (37768319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ecb5efc20fa2f7f4979087b21c53912ef2ca08440fc59f6f45a08110cf5c7a`  
		Last Modified: Wed, 25 Jun 2025 19:20:33 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf1976f78ea9da6aac6eca71bba00402ed4e6f70e68f8ceca5769d3145b46a4`  
		Last Modified: Wed, 25 Jun 2025 19:20:37 GMT  
		Size: 948.1 KB (948119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e15ea6651c46852f31032f3be4a96cd0fd81677d02692f08241acfa146fbae`  
		Last Modified: Wed, 25 Jun 2025 19:22:30 GMT  
		Size: 300.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec6e2b21893e5e8df9873a3f0ce5aa28064dd2b2cdd506f972800f82a337563`  
		Last Modified: Wed, 25 Jun 2025 20:01:55 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f8e17800e1e2ffef597568b8ab65a452b2892319699ac8dd36ce599603dee2`  
		Last Modified: Thu, 26 Jun 2025 01:03:31 GMT  
		Size: 107.7 MB (107682673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5913635ba25860a09292aafbcd3506a600500d08858f16db49c296258e5c98`  
		Last Modified: Wed, 25 Jun 2025 20:01:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f54a9cc7f34506304072faadb11f98567d67f84901b7b81c2af5c6ff7209850`  
		Last Modified: Wed, 25 Jun 2025 20:02:01 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1a846cb133237cdbac987016cf378d941669a8e53b2396892d1e6f7f04c051`  
		Last Modified: Wed, 25 Jun 2025 20:02:06 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:10b0192d5cb568f89a81b698779a294b1b5543537e4c6fc0f56924dc47b3e915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514df50739565456545e6ab15f087d15d8d0b00a75883603bbd614278267fdaa`

```dockerfile
```

-	Layers:
	-	`sha256:ca2da039098dc2a6df2287f541845e82515d185a1da58448277d1095c18ca33f`  
		Last Modified: Wed, 25 Jun 2025 21:36:12 GMT  
		Size: 4.1 MB (4140842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4050928bc1c270e0aec887a0887bcb48250f6dae500ef65121cb03e98bb8237c`  
		Last Modified: Wed, 25 Jun 2025 21:36:13 GMT  
		Size: 30.8 KB (30774 bytes)  
		MIME: application/vnd.in-toto+json
