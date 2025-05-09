## `mariadb:10-ubi`

```console
$ docker pull mariadb@sha256:8b32a4cb71ab1aba413b075086f0df8eb1880a5e8de68bbaadf1726c88712c46
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
$ docker pull mariadb@sha256:443139f07c0ee4760667d8fea34bbc19fc2ca356ae8cd7fc22ead1dd7c498be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.6 MB (146622275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312a2051fea12a59afdea6faa15c9b849cec14d90a228fc0a10187d9724a2b7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL url="https://www.redhat.com"
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL io.openshift.expose-services=""
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 05 Feb 2025 21:06:18 GMT
ENV container oci
# Wed, 05 Feb 2025 21:06:18 GMT
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 21:06:18 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Wed, 05 Feb 2025 21:06:18 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENV GOSU_VERSION=1.17
# Wed, 05 Feb 2025 21:06:18 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.11 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.11 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 05 Feb 2025 21:06:18 GMT
ARG MARIADB_VERSION=10.11.11
# Wed, 05 Feb 2025 21:06:18 GMT
ENV MARIADB_VERSION=10.11.11
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: MARIADB_VERSION=10.11.11
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: MARIADB_VERSION=10.11.11
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 21:06:18 GMT
USER mysql
# Wed, 05 Feb 2025 21:06:18 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b91ae3d7d9a095dbc2ef7ba5dbdbaa9af533c10965b7f498259fc741b613b5`  
		Last Modified: Thu, 08 May 2025 17:05:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036cf5c6c992a148944ac4b43cb0d0d27752f2471c8d47a2bd6505afd298dc9a`  
		Last Modified: Thu, 08 May 2025 17:05:50 GMT  
		Size: 983.5 KB (983465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dac591f9ed3604c101ec0f35247c9a8d7d5c515dfdb1dc3e84d3e40ddce8b87`  
		Last Modified: Thu, 08 May 2025 17:05:50 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f9d2071106ad6a7f75a7ba32c55f411cc66caf2ff4e6c8809617ef3f4fee1`  
		Last Modified: Thu, 08 May 2025 17:05:51 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520ced1ae8d3bb3dadc9da13adf38fde01bacd6c760ffc256db517c5bef3b1ff`  
		Last Modified: Thu, 08 May 2025 17:06:01 GMT  
		Size: 105.9 MB (105910222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f7651c103660dbad446ed3e45c47f8f01fabef1009032ee2a40f9b421d595e`  
		Last Modified: Thu, 08 May 2025 17:05:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43a9ad4638cd39868981a004ae784f0e76eff32a7cac2df6691791ec71eb9b6`  
		Last Modified: Thu, 08 May 2025 17:05:51 GMT  
		Size: 4.0 KB (4017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317b52068c2c6ded14a598cc11f04acb6c9efb80e047ae9801d65ef54df6c1f5`  
		Last Modified: Thu, 08 May 2025 17:05:51 GMT  
		Size: 8.4 KB (8368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:8d35b3919f9e6c245142743bbe5d27907c46a625062d75bcd260394340774123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0718e294f1718a68c7ee077dc31affb318f73620ba834206fc67f1951046979`

```dockerfile
```

-	Layers:
	-	`sha256:a76efa63a806fdf651d05ccf42fbfb7d762273ae8c762c3f4645740c267d8c41`  
		Last Modified: Tue, 29 Apr 2025 16:39:51 GMT  
		Size: 4.1 MB (4089717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aead0ad6f96150fa01051c7bd34b8aef56e48d912aa35fbcf66197dcdc86651`  
		Last Modified: Tue, 29 Apr 2025 16:39:50 GMT  
		Size: 30.2 KB (30195 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f54b5f7aa4783204f0e3bb476877181cf4d1fdbdf8d5974434d2b438fbe91cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143114136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9ab47d00de3e1ad918c4cf2642ea3291847dab88fdc067864d1c92b039f067`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL url="https://www.redhat.com"
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL io.openshift.expose-services=""
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 05 Feb 2025 21:06:18 GMT
ENV container oci
# Wed, 05 Feb 2025 21:06:18 GMT
COPY dir:37e2781211ed66b85e838f75f63c4036aeedc358075b7ac677bbe4ad43998692 in / 
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 21:06:18 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL "build-date"="2025-04-28T15:48:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Wed, 05 Feb 2025 21:06:18 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENV GOSU_VERSION=1.17
# Wed, 05 Feb 2025 21:06:18 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.11 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.11 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 05 Feb 2025 21:06:18 GMT
ARG MARIADB_VERSION=10.11.11
# Wed, 05 Feb 2025 21:06:18 GMT
ENV MARIADB_VERSION=10.11.11
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: MARIADB_VERSION=10.11.11
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: MARIADB_VERSION=10.11.11
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 21:06:18 GMT
USER mysql
# Wed, 05 Feb 2025 21:06:18 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:2aa6bd15812764b98217de512ddcd6b7fc8cb96437e1fa30d7963118dce559ff`  
		Last Modified: Thu, 08 May 2025 17:05:40 GMT  
		Size: 37.9 MB (37887470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf3cf15a2e16ff27f49875c9bc079b1dda0ecab35ed92cefabe36bd8d714f2a`  
		Last Modified: Thu, 08 May 2025 18:09:47 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526c3cfea58204dec9d2a30ebe4456de42bb00a28e1969530bf0bc7c41316b46`  
		Last Modified: Thu, 08 May 2025 18:09:48 GMT  
		Size: 913.8 KB (913810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcda6594ce9049d902755dc5597761affb0c2e1ab7ef6ee2fad74b4b7dd83c16`  
		Last Modified: Fri, 09 May 2025 00:38:19 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16bc8997134ea80d09eeb06f90e90ca6da8247876b61f44546684626310b03c`  
		Last Modified: Fri, 09 May 2025 00:38:18 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67698a9b29e6f81e7a52c6729558928e022794daaa1145ca02a043fe62605781`  
		Last Modified: Fri, 09 May 2025 00:38:31 GMT  
		Size: 104.3 MB (104298825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3e1d6cd1517f80cc39c068e7606f8676fa5fd4681fddc8cd7d0e524f712da5`  
		Last Modified: Fri, 09 May 2025 00:38:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77680e94134cd4a127e7ed1f2d450018d87abfabb6f48eaa722cf31e7bfa6d16`  
		Last Modified: Fri, 09 May 2025 00:38:18 GMT  
		Size: 4.0 KB (4019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9569115d4b8b58b8c42cff8a18b96c24a248d65905abac725a191920456b0571`  
		Last Modified: Fri, 09 May 2025 00:38:18 GMT  
		Size: 8.4 KB (8368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:c30aaee57270be33849ce879fc5e8e874c5b847ab16a806b14fd799764f14ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a7e8cf630589388783b99bcc23e08429d02967722bba5634f4da180504bd7d`

```dockerfile
```

-	Layers:
	-	`sha256:776347eeace05f1f14928349f220e24ca31f4c3e437757c8625f3ba44b6d6719`  
		Last Modified: Tue, 29 Apr 2025 18:00:05 GMT  
		Size: 4.1 MB (4089582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d2ee561ef37a77159db5d9ddf1c3c8558c53b67ca1b3b1c17979ae834b435ac`  
		Last Modified: Tue, 29 Apr 2025 18:00:05 GMT  
		Size: 30.4 KB (30362 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1308c33abca1b768f462fa1c894b30d2bbeab521d5c47f9e99500fbc98c7262d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (156968835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f744e73fe4be23e65a8fee8b58bd69ee3f4b06edc00d2ac8b8a1c441b7811776`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL url="https://www.redhat.com"
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL io.openshift.expose-services=""
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 05 Feb 2025 21:06:18 GMT
ENV container oci
# Wed, 05 Feb 2025 21:06:18 GMT
COPY dir:352b288c8223eaef7c671c611c93e11c1f1a08ec40f3f05f199babc323ce9c37 in / 
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 21:06:18 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL "build-date"="2025-04-28T15:57:47" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Wed, 05 Feb 2025 21:06:18 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENV GOSU_VERSION=1.17
# Wed, 05 Feb 2025 21:06:18 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.11 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.11 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 05 Feb 2025 21:06:18 GMT
ARG MARIADB_VERSION=10.11.11
# Wed, 05 Feb 2025 21:06:18 GMT
ENV MARIADB_VERSION=10.11.11
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: MARIADB_VERSION=10.11.11
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: MARIADB_VERSION=10.11.11
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 21:06:18 GMT
USER mysql
# Wed, 05 Feb 2025 21:06:18 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e32416660495649b2ba0129e756351f46ec1023f3bc9594febaf780fbab240ec`  
		Last Modified: Thu, 08 May 2025 17:53:37 GMT  
		Size: 44.1 MB (44107495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c167dac3fe92ecfcb184985f914783d520d0e03556ed940b448c2e3fa4354a`  
		Last Modified: Tue, 29 Apr 2025 18:51:09 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a94a7f624c567f8270b20b6d091e2a840ab796d5e4e46ea739e692614eafe8`  
		Last Modified: Tue, 29 Apr 2025 18:51:09 GMT  
		Size: 904.3 KB (904316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de03c23c15b632e1a8bfe36b2f790f02814631060a7fd249e9158e261d0c7fa8`  
		Last Modified: Tue, 29 Apr 2025 18:56:14 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1af3c85b4d4c0d282bd0bbeb2a3dc4f7ede0e2df57200818f9f1e467eba3a0`  
		Last Modified: Tue, 29 Apr 2025 18:56:15 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3419eacac96d50065a6ae1c473763e83e1b65328e30fe415bfa438a0a283f64b`  
		Last Modified: Tue, 29 Apr 2025 18:56:18 GMT  
		Size: 111.9 MB (111942989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17217955a289fedfc24436da137804019fb0e197b53c2fa6bdcd71f404e4f524`  
		Last Modified: Tue, 29 Apr 2025 18:56:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ecb12f7cf6e7b309500def21ae8d3d8fb72b00ebc577b86b38a46e4bad0fa9`  
		Last Modified: Tue, 29 Apr 2025 18:56:16 GMT  
		Size: 4.0 KB (4016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3a4d042d33ac4a2dd4930d8c208ceeea8a37e8da2149c4fb6a64101256dbb6`  
		Last Modified: Tue, 29 Apr 2025 18:56:16 GMT  
		Size: 8.4 KB (8366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:405536b9a4c59b45627f3f24a1bce1f7f44a04026780ed75d131b080495286d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980da0ac511553d5839ff6372cd14b8d4056e2a4e911d15355560fff33889a3a`

```dockerfile
```

-	Layers:
	-	`sha256:2dce3b7524764034c3176c2815d99ede9aa5b2f0552741f0e0aa6afb2a8255c7`  
		Last Modified: Tue, 29 Apr 2025 18:56:15 GMT  
		Size: 4.1 MB (4090809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96c6e6980a7731b6a552e3ed3dd1d8db2d45c4ae1eff4af6678bf4e1481751af`  
		Last Modified: Tue, 29 Apr 2025 18:56:14 GMT  
		Size: 30.2 KB (30249 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:db720f891d6dd672deec5a80160c505037f112eec47c6804560f1344732fc3f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145319577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea47ff73ad600f8743204bba410a049a101407a983b87f8bcf66ab4df9758fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL url="https://www.redhat.com"
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL io.openshift.expose-services=""
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 05 Feb 2025 21:06:18 GMT
ENV container oci
# Wed, 05 Feb 2025 21:06:18 GMT
COPY dir:bab1dba8fd7b792fd9c8b4d4831f07de632d98b60b25b5bfb612394258ecf142 in / 
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 21:06:18 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL "build-date"="2025-04-28T15:49:27" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Wed, 05 Feb 2025 21:06:18 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENV GOSU_VERSION=1.17
# Wed, 05 Feb 2025 21:06:18 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.11 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.11 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 05 Feb 2025 21:06:18 GMT
ARG MARIADB_VERSION=10.11.11
# Wed, 05 Feb 2025 21:06:18 GMT
ENV MARIADB_VERSION=10.11.11
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: MARIADB_VERSION=10.11.11
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: MARIADB_VERSION=10.11.11
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Feb 2025 21:06:18 GMT
USER mysql
# Wed, 05 Feb 2025 21:06:18 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0a17b1176e4d1360a16f39111ed35c973d6f8d1a50962dc023a27e6fbfb36505`  
		Last Modified: Thu, 08 May 2025 17:53:37 GMT  
		Size: 37.8 MB (37826548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b0080508734a7c6e027f54b6723530b3d3ae43c6af53af72a5daa0067ee10a`  
		Last Modified: Tue, 29 Apr 2025 19:23:06 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a0f5f3a689b1ec8a54a7433d1a00161a82e2603afa578666ca406b8c998624`  
		Last Modified: Tue, 29 Apr 2025 19:23:06 GMT  
		Size: 948.1 KB (948118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa3e1d322dcf293ca1fc8be90d587a8c0b83924709bd33088f7090aa99148ca`  
		Last Modified: Tue, 29 Apr 2025 19:26:37 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97f12430160c0fb5016a704c3122a65bd0d736c4f253eee4de571138fb316cf`  
		Last Modified: Tue, 29 Apr 2025 19:26:37 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372942c11bd649e7a68fc5c4229b6364edac49e5ebfcff4d62693765766fde20`  
		Last Modified: Tue, 29 Apr 2025 19:26:39 GMT  
		Size: 106.5 MB (106530878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcc2fdd5c2aff20d73257cfcedf3b441bd992afd24e31406d07eb543bd144e9`  
		Last Modified: Tue, 29 Apr 2025 19:26:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c277925ea2a62463dea1b4cbb97f0dff88df7ca4b118a964eb3a6c224d781a`  
		Last Modified: Tue, 29 Apr 2025 19:26:38 GMT  
		Size: 4.0 KB (4020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57da9232b6d50a89e970edae365542cb4d9cbaff15b94c0023ad1b648f26307b`  
		Last Modified: Tue, 29 Apr 2025 19:26:38 GMT  
		Size: 8.4 KB (8368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:2da5775f9655664891428af8bdbb4ec23fdd178a63715fb1e9eed56c62cad0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafb45c8114bd7e1df5dfc8dbdc418a5a2c93463b52e7f8ae9e1d3e4ca2604de`

```dockerfile
```

-	Layers:
	-	`sha256:f033948e92652321d0825e89373bc6013ea7fa47de5ac0c812b0ce4dda924b98`  
		Last Modified: Tue, 29 Apr 2025 19:26:37 GMT  
		Size: 4.1 MB (4090794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25559dcddb7bea7343c4a21aaf4da431603e7d67fe91138ac6895a54ac6ecfdb`  
		Last Modified: Tue, 29 Apr 2025 19:26:37 GMT  
		Size: 30.2 KB (30194 bytes)  
		MIME: application/vnd.in-toto+json
