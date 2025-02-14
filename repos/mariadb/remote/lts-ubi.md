## `mariadb:lts-ubi`

```console
$ docker pull mariadb@sha256:d336b5260b4e471c68e72d5e6ed2c7e53927e6ef35de65035ce0b4b1f4cf22ae
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
$ docker pull mariadb@sha256:6b6523acdeab82f5b77225ca9673afeab8a7bc02ebcac2394e19d9d67ce2e44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.6 MB (146591230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def8b1130a12561305786d6c604ffe5d20c7b87f808efdbd53e452f1b21b8262`
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
COPY dir:0423d0cd4a34047821e55a2806cb02fc682f017fba03e4344223878a61041986 in / 
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 21:06:18 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL "build-date"="2025-02-13T04:19:45" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
# Wed, 05 Feb 2025 21:06:18 GMT
RUN /bin/sh
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
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 05 Feb 2025 21:06:18 GMT
ARG MARIADB_VERSION=11.4.5
# Wed, 05 Feb 2025 21:06:18 GMT
ENV MARIADB_VERSION=11.4.5
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: MARIADB_VERSION=11.4.5
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: MARIADB_VERSION=11.4.5
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
	-	`sha256:3333307dcd2e4279579646a05a5f99082a61a20906175240445b0e15f73b6d6e`  
		Last Modified: Thu, 13 Feb 2025 06:13:39 GMT  
		Size: 39.4 MB (39366553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5025173ec0b35686a33458b367c2a6e898c824f57a07925c25d26a0cfb5f2e50`  
		Last Modified: Thu, 13 Feb 2025 06:13:37 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affabdf90d9e031c0ac6d1d8e1e79b14b7daeaf74c43173ffa0b8185eb748a0c`  
		Last Modified: Fri, 14 Feb 2025 01:36:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148e6b2aaac2d556839ddab7dbda0d63f9d3f2d576d8c5fc6374b6d06455fb87`  
		Last Modified: Fri, 14 Feb 2025 01:36:48 GMT  
		Size: 983.5 KB (983460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fd1df49b3d3bcd21bffb86a3d97504528ec44a2af07b3eb08f4983aec97621`  
		Last Modified: Fri, 14 Feb 2025 01:27:56 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abaac45dce3ae8c1db9a9bbfe196f54f2710954b38ec0c16a2c3f6bdfb64421e`  
		Last Modified: Fri, 14 Feb 2025 01:27:59 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803d90b96e67c9e7063e7e7fc2c762ed2bb21fc99af8534e439d4c52053758b7`  
		Last Modified: Fri, 14 Feb 2025 01:36:54 GMT  
		Size: 106.2 MB (106226658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838622e2d32326f3b0e4b6572ee4af5770b8549d91ff8537f3522e2952a66910`  
		Last Modified: Fri, 14 Feb 2025 01:36:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488b844d2b5798148977cc52bcdb61f73331d12f08d7ebe39a86c3cd92dd0870`  
		Last Modified: Fri, 14 Feb 2025 01:28:01 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88839655fd3b72d406d1f88de2f5eb3f9d8eef0a1c09a9378d772feadb49039`  
		Last Modified: Fri, 14 Feb 2025 01:28:03 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:4affa0b24d394bdd652978e8062d542b218ae7c9f8e3cb53ff6c4fc07c718210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4101504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24f50f837726921d826b304c4ad6056ff6b92ef329503f7c6dc8ad758f1ad8a`

```dockerfile
```

-	Layers:
	-	`sha256:af2486aa33adf7d794e54aeb1ead3b031cd132f3448a48e3c647a18911e8ff27`  
		Last Modified: Fri, 14 Feb 2025 01:36:24 GMT  
		Size: 4.1 MB (4069946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d8e2c5f478b9355469cffb58fdfcc052645139c12738b65909907ac821a9225`  
		Last Modified: Fri, 14 Feb 2025 01:36:24 GMT  
		Size: 31.6 KB (31558 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:fad5114543032deab0652b8639831e7ee4ec7bb45703158ad7d1924948dfbb7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143099772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4838095cc3ece3655858af6b8a652d00867ac70f1b42a439959c78c9321a8aa`
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
COPY dir:5809c16e2c5c048de6a8d8eea9437ac183b7d2503e26b24a2422ead5736aecad in / 
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 21:06:18 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL "build-date"="2025-02-13T04:25:01" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
# Wed, 05 Feb 2025 21:06:18 GMT
RUN /bin/sh
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
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 05 Feb 2025 21:06:18 GMT
ARG MARIADB_VERSION=11.4.5
# Wed, 05 Feb 2025 21:06:18 GMT
ENV MARIADB_VERSION=11.4.5
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: MARIADB_VERSION=11.4.5
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: MARIADB_VERSION=11.4.5
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
	-	`sha256:1a974ca03628a12f175e2e870c0dc2ca11a5bdb0f7fa02604caaf4dbddec85f3`  
		Last Modified: Fri, 14 Feb 2025 01:37:46 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7944f04e09e0127a922a8aa47b2864804663d61b6fcea2a096e0c871567b8b96`  
		Last Modified: Fri, 14 Feb 2025 01:37:46 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c0d7ec2d410a28042792a3d7abd2ce46bac46fe7ae531953b98590e0f3fa67`  
		Last Modified: Fri, 14 Feb 2025 01:37:51 GMT  
		Size: 104.5 MB (104545356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4896d14b50fb26ebfd433362d8ec9b3c927cd7e245e0dcdb11dd3be22cbe85`  
		Last Modified: Fri, 14 Feb 2025 01:37:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6755901eec3e07f15f1d0350bcd6cdbc2b8f83662aec0847e3f22e99f0720fec`  
		Last Modified: Fri, 14 Feb 2025 01:37:45 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e0a074350e213da067167d7279d431e0c676759eee9b5401473791f0a8b7e7`  
		Last Modified: Fri, 14 Feb 2025 01:37:45 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:f5c6917d67d7890d4ddb07ac7a483649e20f4565c8e9a64826e4028d847b9010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4101536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4520ecf851384e0be50e01c6ba29ed8a941c7797fa496e08bdca7054e4fb4811`

```dockerfile
```

-	Layers:
	-	`sha256:7fa459c46ffd66122c1ba0b0ca934f82b7e798844bf7e7e16b017cb2f8bbaddf`  
		Last Modified: Fri, 14 Feb 2025 01:36:26 GMT  
		Size: 4.1 MB (4069811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22659d27bca836a312986ed09fed0eb03df4c53b928d52619bd7799260197d90`  
		Last Modified: Fri, 14 Feb 2025 01:36:27 GMT  
		Size: 31.7 KB (31725 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9df252eb3e609339f1734bba7d4da877f464abd16c3ff497a0cbfac9dd704eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157013782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89566e71992df91ca61f3b9333bc4c67c7846f656a0a1e0e6ba05515b85f42a9`
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
COPY dir:2c0c7900d5f6c40d02b1787c7aed15027e6a404d210587076552b87add6a3c87 in / 
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 21:06:18 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL "build-date"="2025-02-13T04:27:14" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
# Wed, 05 Feb 2025 21:06:18 GMT
RUN /bin/sh
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
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 05 Feb 2025 21:06:18 GMT
ARG MARIADB_VERSION=11.4.5
# Wed, 05 Feb 2025 21:06:18 GMT
ENV MARIADB_VERSION=11.4.5
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: MARIADB_VERSION=11.4.5
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: MARIADB_VERSION=11.4.5
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
	-	`sha256:66d01604bdabba1da7471f9f16d66bb8cf8fa5528b58ba81228651f0ffe2e009`  
		Last Modified: Fri, 14 Feb 2025 01:26:31 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab722b16a74dba20721a91512a792b3a8fe817020aa644de9e90ee49553b6d9`  
		Last Modified: Fri, 14 Feb 2025 01:26:34 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6a382d7100325e9a4b214531464ba94f980eeede60b8ec9279ec42b1fe73b6`  
		Last Modified: Fri, 14 Feb 2025 02:06:51 GMT  
		Size: 112.3 MB (112317244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e096bac2178e2f563b7d95bffae7275a210482addf274295bf923ecfc5d859e`  
		Last Modified: Fri, 14 Feb 2025 02:06:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b2834094892ebbfdfb4c02be0c0f494d8cc9fa3d056f0b1d6ad6e5f29cae7f`  
		Last Modified: Fri, 14 Feb 2025 01:26:37 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895a4b908319b95dd147e6d06765d51c04f0e0b8d09e0cb33086be54cd22c544`  
		Last Modified: Fri, 14 Feb 2025 01:26:39 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:742237c94199a3cd2b8633b141439ca2ef56370bd319e1b7f2a14227bca4dfdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7d6a63dc03f5dce95d8997c991df4eb8f923791dee06df4066172fbeb78cbf`

```dockerfile
```

-	Layers:
	-	`sha256:fc4ec89bcef47f7925fc419069b52614b9ffa58b634fdef23ff5355f4d7092e4`  
		Last Modified: Fri, 14 Feb 2025 01:36:29 GMT  
		Size: 4.1 MB (4071014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdd2393ffd5d53537c0504c4fdfe9a3303c4ad2ff6639ec01763406e664351aa`  
		Last Modified: Fri, 14 Feb 2025 01:36:29 GMT  
		Size: 31.6 KB (31614 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:091b42ef29e84f354d6bddc4171fc15a7c5bb1c7fd340ae9939f6388fafc25d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145277488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d01d9f6902a2bda717e70c9b8caf64060a0ccf362c53c50f3433d2a9fe15b5c`
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
COPY dir:86825579d6c6c7e4802643396fb14124acbbf3b24f22947be66f890a734b7e7b in / 
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 21:06:18 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL "build-date"="2025-02-06T04:49:32" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
# Wed, 05 Feb 2025 21:06:18 GMT
RUN /bin/sh
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
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 05 Feb 2025 21:06:18 GMT
ARG MARIADB_VERSION=11.4.5
# Wed, 05 Feb 2025 21:06:18 GMT
ENV MARIADB_VERSION=11.4.5
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: MARIADB_VERSION=11.4.5
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Wed, 05 Feb 2025 21:06:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 05 Feb 2025 21:06:18 GMT
# ARGS: MARIADB_VERSION=11.4.5
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
	-	`sha256:dff3dae8634485c4d1f14243b55a740b473ee901b87cfd847a4234dc5a1b876d`  
		Last Modified: Thu, 06 Feb 2025 07:04:17 GMT  
		Size: 37.5 MB (37509515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ba975a618e9922cb358fe027051fa5621498ddb470d175378812c757e5d91c`  
		Last Modified: Thu, 06 Feb 2025 07:04:18 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c1b34dc958985d4a4954da53e2417026ed3f1d5d30320f1d45992b785f8b60`  
		Last Modified: Fri, 07 Feb 2025 08:51:05 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67386ee2c2d6d7395a2baf473710a745f731edad61ee3db2cff6b7c06254e202`  
		Last Modified: Fri, 07 Feb 2025 15:38:52 GMT  
		Size: 948.1 KB (948117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed950d8e5a51ecb71e4877e29a6d6a28bf9ec2c880c8198c031bad1cf235eaf5`  
		Last Modified: Fri, 07 Feb 2025 08:51:07 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b6195d647aa5796a4751db576033978778bace0e080bfa7c4c8ee7d8276912`  
		Last Modified: Fri, 07 Feb 2025 08:51:10 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1d546bfde17354d7e7a26316efb4b91c8b9a9cacfe6b54f8b235f7b5370f8c`  
		Last Modified: Fri, 07 Feb 2025 13:31:05 GMT  
		Size: 106.8 MB (106805298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d821d899a6befa176a4e6283c4330e3b5bfc6d4357df45f762e2f74d3a0fa843`  
		Last Modified: Fri, 07 Feb 2025 08:51:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432140f4a666f8209b9b276702d6207efd19a96ab3e81151b3dd9c3555227cdb`  
		Last Modified: Fri, 07 Feb 2025 08:51:50 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24cb2cfe574532131ce7b028da4914267e8b604f41bdf71a856dd5cb2cb4b97`  
		Last Modified: Fri, 07 Feb 2025 08:51:53 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:2083e35a54a1d816f1625d7f895f517defc2a44e1e89a2f045ae9fdc2c6a1e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ceb4b27b217bb46898e55027601961a626e45beb467ad5c371e2136995c06f`

```dockerfile
```

-	Layers:
	-	`sha256:c51681ac44766789c128051f00092a6be2057cdc7a20c10ad53d9b5e10127edd`  
		Last Modified: Tue, 11 Feb 2025 04:05:56 GMT  
		Size: 4.1 MB (4070971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d08a3177f8268bddac57a037eccd4ad3c924408dd932f47f0cc2b20a3cf237a1`  
		Last Modified: Sat, 08 Feb 2025 02:31:39 GMT  
		Size: 31.6 KB (31558 bytes)  
		MIME: application/vnd.in-toto+json
