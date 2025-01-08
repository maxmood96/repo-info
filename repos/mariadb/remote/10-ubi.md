## `mariadb:10-ubi`

```console
$ docker pull mariadb@sha256:495166ca5918ea547588bbc96d2c4dc68a9b1133aff26b1970308f8fb5db8377
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

### `mariadb:10-ubi` - linux; amd64

```console
$ docker pull mariadb@sha256:2b30b533249256768b348d6bf5526f1f0e5641d74e625fa754a3fbe11a2545f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (145959694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1724b4d2437aded7aa21c6583c7b8113200151e79e1bff17dd9155642aee40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL url="https://www.redhat.com"
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 Nov 2024 20:52:12 GMT
ENV container oci
# Mon, 04 Nov 2024 20:52:12 GMT
COPY dir:0485e287b26ef73c199c820b8915015ba33a659f620dc17eafe7e7a33f8bf780 in / 
# Mon, 04 Nov 2024 20:52:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 04 Nov 2024 20:52:12 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 20:52:12 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL "build-date"="2024-12-18T04:56:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
# Mon, 04 Nov 2024 20:52:12 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 20:52:12 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.10 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.10 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 04 Nov 2024 20:52:12 GMT
ARG MARIADB_VERSION=10.11.10
# Mon, 04 Nov 2024 20:52:12 GMT
ENV MARIADB_VERSION=10.11.10
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: MARIADB_VERSION=10.11.10
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: MARIADB_VERSION=10.11.10
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Nov 2024 20:52:12 GMT
USER mysql
# Mon, 04 Nov 2024 20:52:12 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 04 Nov 2024 20:52:12 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:1e6b7297048ae70484705dda4e582fb8ad5778ea4c8ae464cf3e6a02ac439012`  
		Last Modified: Wed, 18 Dec 2024 06:15:23 GMT  
		Size: 39.4 MB (39432409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe308e47e5efb01aa676dea2124482684b6cf07d5a9c45992eee496f24c5351`  
		Last Modified: Thu, 19 Dec 2024 06:28:02 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c1377b199099e01f9a6897b1845d3c200f31d1e38a10451336a95d0ebe9762`  
		Last Modified: Thu, 19 Dec 2024 06:28:02 GMT  
		Size: 983.5 KB (983467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e6f0d48631a84096c231a54cd4a46f1fc5a113b99d16dce813bdfcb961fa3a`  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf52b447dba4f652fcde22cd0ce321db447257d87af967a906e2527413e5da11`  
		Last Modified: Thu, 19 Dec 2024 06:28:02 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e00195092a0023a5d914226db3cbc8824da884e95539e8dca765c8dbf76cf9a`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 105.5 MB (105529785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab2499c71f9baa64dfde2dd4cb3b4f260462f3af065556b32b221ef5eb336ae`  
		Last Modified: Thu, 19 Dec 2024 06:28:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52589690a0c9b79744273867bd2b0bce77a615f9967fb0054cf1bb920d78e986`  
		Last Modified: Thu, 19 Dec 2024 06:28:03 GMT  
		Size: 4.0 KB (4018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5885e4aebb81e71aea14fb7481822a888a8ffea7755d3a4ea2330781d7c98ca8`  
		Last Modified: Thu, 19 Dec 2024 06:28:03 GMT  
		Size: 8.4 KB (8364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:b31f479cc01e09ee8ab6271be1c9ee03f01682645a7cd2302b8c725f20c4bc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee6e98c5a0217d0dae1fee50971a667e9d6658eea41b905dd4a4ba7df6eb3d1`

```dockerfile
```

-	Layers:
	-	`sha256:6e9252462e5a5c1dddcadbf758ffc85cded378cd764484411eae68b264abb369`  
		Last Modified: Thu, 19 Dec 2024 06:28:02 GMT  
		Size: 4.0 MB (4021074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b3ef3af16330750be42f6deaa765bdd7834de50c6e9e71a94151084c02c65d9`  
		Last Modified: Thu, 19 Dec 2024 06:28:02 GMT  
		Size: 30.2 KB (30154 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:9e267cdc569b7476f65812d20fc57399454ab05a17f805095526994a210bcbb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142377655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81cc78baf9c54c6a3f0316b5637d8e4303590cac8bb6c154456fe1aff7019db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL url="https://www.redhat.com"
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 Nov 2024 20:52:12 GMT
ENV container oci
# Mon, 04 Nov 2024 20:52:12 GMT
COPY dir:2b8ad1e81974d4feec292500267d9d72634438f9ec07a466db827a8114ef0993 in / 
# Mon, 04 Nov 2024 20:52:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 04 Nov 2024 20:52:12 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 20:52:12 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL "build-date"="2024-12-18T05:01:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
# Mon, 04 Nov 2024 20:52:12 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 20:52:12 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.10 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.10 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 04 Nov 2024 20:52:12 GMT
ARG MARIADB_VERSION=10.11.10
# Mon, 04 Nov 2024 20:52:12 GMT
ENV MARIADB_VERSION=10.11.10
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: MARIADB_VERSION=10.11.10
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: MARIADB_VERSION=10.11.10
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Nov 2024 20:52:12 GMT
USER mysql
# Mon, 04 Nov 2024 20:52:12 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 04 Nov 2024 20:52:12 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:3415b32764d8c185fafcd0c946a41d5028c72a76a1c10bcd8690f139ff79eb40`  
		Last Modified: Wed, 18 Dec 2024 06:15:28 GMT  
		Size: 37.6 MB (37577418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddd2646963cf55c51258516a47ad51722be951ad64cc336917b609bf4842b9b`  
		Last Modified: Thu, 19 Dec 2024 06:37:30 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b6033037830a49822327c9a17cb5d407e0eeaa9e46e326ff0e27aa08ed34b7`  
		Size: 913.8 KB (913801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a9ec3d4b80bacf4f0cf6e2dba1bec28dac02bf199e56a6a975954954df9417`  
		Last Modified: Thu, 19 Dec 2024 06:42:53 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1925bed469b5ef710e8e8a497fad7c4d51db0a80c6ba1add3a460f87f78e225`  
		Last Modified: Thu, 19 Dec 2024 06:42:53 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0215f962975aa15acb04ecc40c827212cdbee764a726f6f3b3b448abba20e9ca`  
		Last Modified: Thu, 19 Dec 2024 06:42:56 GMT  
		Size: 103.9 MB (103872404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08b54b181050e895d3c82f77fc37967a78295ddfad017cd8456a6be77fd2967`  
		Last Modified: Thu, 19 Dec 2024 06:42:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db209867317f5054d6fc873fafc4ba1a79fb9fbf03f451e19d46ea54d17f561`  
		Last Modified: Thu, 19 Dec 2024 06:42:54 GMT  
		Size: 4.0 KB (4019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e32e946c1edbc82386ba4835f7d24d1494f4aee95ae779875f0c9532139e21`  
		Last Modified: Thu, 19 Dec 2024 06:42:54 GMT  
		Size: 8.4 KB (8365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:5fd4969549c8a7d313c4e2a483763a0655091807f9f4ae177d0b7e45dc3f84b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a96b6b897b78cde72656fc2b0eef55bfa5b82d7e4b301a4ab08e561eeafd9f`

```dockerfile
```

-	Layers:
	-	`sha256:80079504a8633f69126035a495e9f6f237a03e295a65fef4c0a6074e19c1b02c`  
		Last Modified: Thu, 19 Dec 2024 06:42:54 GMT  
		Size: 4.0 MB (4020935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:399cea3fcfdaa7e31e154ad634186c10c67a410806215e471685f47e38146c38`  
		Last Modified: Thu, 19 Dec 2024 06:42:53 GMT  
		Size: 30.3 KB (30322 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:620ed5ca267329b3266b82a4be5fa6519e9cd4ea8cf7b962bef9cece98422ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156260448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266065666cfb24613932c53bb14120ae19387c4f8217a9e722c9da37de18eddf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL url="https://www.redhat.com"
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 Nov 2024 20:52:12 GMT
ENV container oci
# Mon, 04 Nov 2024 20:52:12 GMT
COPY dir:812543eca6d750875f0aa085b69e2a0865cd4978afc12d0f5ee611cc97abcc57 in / 
# Mon, 04 Nov 2024 20:52:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 04 Nov 2024 20:52:12 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 20:52:12 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL "build-date"="2024-12-18T05:08:50" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
# Mon, 04 Nov 2024 20:52:12 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 20:52:12 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.10 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.10 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 04 Nov 2024 20:52:12 GMT
ARG MARIADB_VERSION=10.11.10
# Mon, 04 Nov 2024 20:52:12 GMT
ENV MARIADB_VERSION=10.11.10
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: MARIADB_VERSION=10.11.10
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: MARIADB_VERSION=10.11.10
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Nov 2024 20:52:12 GMT
USER mysql
# Mon, 04 Nov 2024 20:52:12 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 04 Nov 2024 20:52:12 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:08256d51c6c275f4c9f694d18b8f1c909073b012ba7c7d9b5ea9f948ab194c83`  
		Last Modified: Wed, 18 Dec 2024 06:15:40 GMT  
		Size: 43.8 MB (43794286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0038cde2c190c05a15347362185472b37226b50c08cb6f0390e30e29ab19b91`  
		Last Modified: Thu, 19 Dec 2024 06:39:51 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7cd1cb4dee3e92a0c5e8a3ad55a35678e878980e4d0ea27ea16d53c4165e84`  
		Last Modified: Thu, 19 Dec 2024 06:39:51 GMT  
		Size: 904.3 KB (904299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63126126225c4e0315c1caa21bc8157b36ca48b8c0b560210a2e5e4729e1c0a`  
		Last Modified: Thu, 19 Dec 2024 06:44:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552eea6976bfbbe58d3bb7fd1321eb615cd5351b511595d311d8f38748cda6ad`  
		Last Modified: Thu, 19 Dec 2024 06:44:53 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5760193ef32d227d105bc42666ecef1ef4706e7cbaa4934842bd5455c3c96cca`  
		Last Modified: Thu, 19 Dec 2024 06:44:56 GMT  
		Size: 111.5 MB (111547826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa191dae56d818d5ca7b4f83ab780675fa9997aea7ce52949f5607464214592`  
		Last Modified: Thu, 19 Dec 2024 06:44:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebaedd34de432b863c6e14a472c87d728590fbaacbe438f63f17d06f6db936e`  
		Last Modified: Thu, 19 Dec 2024 06:44:54 GMT  
		Size: 4.0 KB (4017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d6e83ee703799d26ea50c06108d6533086d35d10f08237e02cd707ff6a2d97`  
		Last Modified: Thu, 19 Dec 2024 06:44:54 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:d03aa1a6270154e44789c7d10395018255400528a26d278ee2fa6a201ec50ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4052372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e21613e4ee461d668dad6727e4d6bc350a83854f7b5ddcd4165e437b4b7a07`

```dockerfile
```

-	Layers:
	-	`sha256:a4cb89c44c7362f970e32e12aa6479accac4861ea3fa528f75eceaa69c359279`  
		Last Modified: Thu, 19 Dec 2024 06:44:54 GMT  
		Size: 4.0 MB (4022162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e46b41baec170b30896697040724040d2676d10792c3984cb3072d36cf00e43`  
		Last Modified: Thu, 19 Dec 2024 06:44:53 GMT  
		Size: 30.2 KB (30210 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:a05d73cc9558713189b12154636cb3c001526bef1e3a653edb6d4f573380d557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144638420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471e313969ee9f176eaa310761493ea601d6a81e07f1fd12171b4544e991315f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL url="https://www.redhat.com"
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 Nov 2024 20:52:12 GMT
ENV container oci
# Mon, 04 Nov 2024 20:52:12 GMT
COPY dir:4cc244bf21ded43360cc8d21bfb3cdbb5e29add2583a06922139bfe953e2576b in / 
# Mon, 04 Nov 2024 20:52:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 04 Nov 2024 20:52:12 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 20:52:12 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL "build-date"="2024-12-18T05:02:28" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
# Mon, 04 Nov 2024 20:52:12 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 20:52:12 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.10 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.10 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 04 Nov 2024 20:52:12 GMT
ARG MARIADB_VERSION=10.11.10
# Mon, 04 Nov 2024 20:52:12 GMT
ENV MARIADB_VERSION=10.11.10
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: MARIADB_VERSION=10.11.10
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: MARIADB_VERSION=10.11.10
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Nov 2024 20:52:12 GMT
USER mysql
# Mon, 04 Nov 2024 20:52:12 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 04 Nov 2024 20:52:12 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:09ca79ad6db051c7cb34adea156f17305f9fe366951ef8100fcdbf06dd0dd31c`  
		Last Modified: Wed, 18 Dec 2024 06:15:33 GMT  
		Size: 37.5 MB (37533376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7d5e6977905585a3eee194536aae023c72e63b0a182101635f6b76e741a43a`  
		Last Modified: Thu, 19 Dec 2024 06:40:11 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be37fea23daf13a30c5b3180ab7a1b10e82b3f198386348da5e90d02a22b2941`  
		Last Modified: Thu, 19 Dec 2024 06:40:12 GMT  
		Size: 948.1 KB (948118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566185417c2c91aa833b3a7e3fcad20e193d5a440c1f4d78c273a664523b6219`  
		Last Modified: Thu, 19 Dec 2024 06:44:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbd8865cb0bf3be6d9e730ac20f5ddc40a427fbfe00d3107da875f90e5f4b5e`  
		Last Modified: Thu, 19 Dec 2024 06:44:55 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2361323d0c39f0cee7e838ee09e35974d3ac7ccc098cbd1beaf59371032bc3e2`  
		Last Modified: Thu, 19 Dec 2024 06:44:57 GMT  
		Size: 106.1 MB (106142887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181b1ce68df10f8b7699962907112b09103945b15f1c351e0625e6e8bb082dcd`  
		Last Modified: Thu, 19 Dec 2024 06:44:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3eb1da6c0dce222fd8f06426f9b26ccfcfde490bb4c034e25788c437e4da85`  
		Last Modified: Thu, 19 Dec 2024 06:44:55 GMT  
		Size: 4.0 KB (4019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782b62c23175197c96fd50f5e7a04c70cafe4b3e319addc712fa0a6130005bc`  
		Last Modified: Thu, 19 Dec 2024 06:44:55 GMT  
		Size: 8.4 KB (8368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:33beb846501101c17ddd85b380f792888c869beca922525a2031eccadd810113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4052302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db59dd1b764a702f5185ba1d93ab300931b8296c9708a008c82f32352048f5a5`

```dockerfile
```

-	Layers:
	-	`sha256:7afd651321eb28b8012fbfe228eed9b11ad9e6204b8aade0dd65b6691d2d957f`  
		Last Modified: Thu, 19 Dec 2024 06:44:55 GMT  
		Size: 4.0 MB (4022147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:522e9fcf087cbb583d1cab406eba9a593fabe55d4f495e22e3a560a6cbab4155`  
		Last Modified: Thu, 19 Dec 2024 06:44:54 GMT  
		Size: 30.2 KB (30155 bytes)  
		MIME: application/vnd.in-toto+json
