## `mariadb:lts-ubi`

```console
$ docker pull mariadb@sha256:e391d60a93de786d9b4c25735d5f557c991ea64adb40877d32cbba625302c3b2
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
$ docker pull mariadb@sha256:dbce0fa4235e42863aa0ebdc9da810a717cb5cfa0a5ec1f444ea6d2c8100cbb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146314387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3cccd80398a5bab5bfa9473ee9bbd75a5f71a1fd14971fb6f259c1e5a408a3`
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
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Mon, 04 Nov 2024 20:52:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 04 Nov 2024 20:52:12 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 20:52:12 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Mon, 04 Nov 2024 20:52:12 GMT
RUN /bin/sh
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
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.4 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 04 Nov 2024 20:52:12 GMT
ARG MARIADB_VERSION=11.4.4
# Mon, 04 Nov 2024 20:52:12 GMT
ENV MARIADB_VERSION=11.4.4
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: MARIADB_VERSION=11.4.4
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: MARIADB_VERSION=11.4.4
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc18dd49c4a96b3da4893b522db0e04087785b2a36d6fc02e8b07cdd11c167b`  
		Last Modified: Sat, 16 Nov 2024 02:09:26 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a065ab0100691c02018eb5fcb0b9c5db98024a66310f34efad8e835293b89c`  
		Last Modified: Sat, 16 Nov 2024 02:09:26 GMT  
		Size: 983.5 KB (983467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e615e8300707e479d19a9ce8d51c47f4aa16f108bba114265158e006d8c776f8`  
		Last Modified: Sat, 16 Nov 2024 02:09:26 GMT  
		Size: 347.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d4f47bf92c76217e44a378b1fdfeb17c41934a3ef5bc7d8c2f3c8158e07434`  
		Last Modified: Sat, 16 Nov 2024 02:09:26 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31496e1a4354a1fce724c148c6b3bca9d5f053238f115df4f1dc6b119217c4a0`  
		Last Modified: Sat, 16 Nov 2024 02:09:28 GMT  
		Size: 105.4 MB (105378488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3498e5945428cb64e7814ce8efbffbe067350e17638ce2806376115b456c7f03`  
		Last Modified: Sat, 16 Nov 2024 02:09:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fca6ed8b8edb94747dcdbaf877f4c8727ca4a7eefc62c00bbb9b3ed2cf723a6`  
		Last Modified: Sat, 16 Nov 2024 02:09:27 GMT  
		Size: 4.0 KB (4040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbe311a7898b9a0f61f423e6d4b6ea582e564a0e012a70a619ed3896fd9b7c0`  
		Last Modified: Sat, 16 Nov 2024 02:09:27 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:46e01b4fba8dc3550c8ae045fe31bd9d52056d3f93fdbdabdbbd70c9273ea96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4069578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ed96105b263d5c4917a7b43859e914107413136799e738a7822353cb6e8f26`

```dockerfile
```

-	Layers:
	-	`sha256:54dd432a1f5c5bca937b1497901d7165540ca9379f1a87b0dc625da906f5afd5`  
		Last Modified: Sat, 16 Nov 2024 02:09:26 GMT  
		Size: 4.0 MB (4038042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26d6c859d8123598125be51b015cc957095e170e5a4cca309df340032f0e1e9c`  
		Last Modified: Sat, 16 Nov 2024 02:09:26 GMT  
		Size: 31.5 KB (31536 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:63139454191430ab028b932a6472e02592abf939037b85f8133fd535857219a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142729947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d880834487e3bc7088e78634358a08583f8b12a49fa55911b3650e45530ec4e1`
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
COPY dir:7fe66f5f8373d1d6b22336da5ccea9872ce92f8e71c6661e555027e35af9fc8d in / 
# Mon, 04 Nov 2024 20:52:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 04 Nov 2024 20:52:12 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 20:52:12 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL "build-date"="2024-11-14T14:10:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Mon, 04 Nov 2024 20:52:12 GMT
RUN /bin/sh
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
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.4 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 04 Nov 2024 20:52:12 GMT
ARG MARIADB_VERSION=11.4.4
# Mon, 04 Nov 2024 20:52:12 GMT
ENV MARIADB_VERSION=11.4.4
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: MARIADB_VERSION=11.4.4
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: MARIADB_VERSION=11.4.4
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
	-	`sha256:06efaada693c8039399aa295b10cf1156c7c64eb4814487ce00c94f0f3312913`  
		Last Modified: Thu, 14 Nov 2024 22:57:54 GMT  
		Size: 38.0 MB (38048586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61b2e9481ca4da337dc5e273b5e6c1e9a053035fb040222bf843ef269dc0699`  
		Last Modified: Thu, 14 Nov 2024 22:57:48 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e32f1a8749960bffeac5b6b26ad7726443c2d081f6fa133970a60024ed6a2c1`  
		Last Modified: Sat, 16 Nov 2024 02:36:47 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8533d85d5345d3da25002a849b9aa2c6a152d756176dd96438a6cf0c1b954b0c`  
		Last Modified: Sat, 16 Nov 2024 02:36:47 GMT  
		Size: 913.8 KB (913810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ef143b63b2873139261ee92d7f54ffffeaa34d6ecc6e370020c415cb51f894`  
		Last Modified: Sat, 16 Nov 2024 02:38:55 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d4434f711c17e6d048717b7380b2f0e90843636fa643860920ecffabba6802`  
		Last Modified: Sat, 16 Nov 2024 02:38:55 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ac71ad6d59ed5fca6a119904e8ca23e14ed23e490768336754fe88bd88b981`  
		Last Modified: Sat, 16 Nov 2024 02:38:58 GMT  
		Size: 103.7 MB (103689865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7350302533cee0837a9c57de19bc2e785d111c401fe4d705d9b2d25a68c78db`  
		Last Modified: Sat, 16 Nov 2024 02:38:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30664cbd3e16f4494d9928280172d916e98188fb92455cc384896d53d503fe`  
		Last Modified: Sat, 16 Nov 2024 02:38:56 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4dc03899e5cc6bbb412431dc1c399108a7a1a947efb45c1d7c4c825547e6a3`  
		Last Modified: Sat, 16 Nov 2024 02:38:56 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:1b1577b1eca29400bee81e6f0341b86a072b5014825abad471cb5c730ccd46ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4069691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2705942d752ee1a9b5aa554e9539e25156ec94bc97050ebab5ccb00f213d938d`

```dockerfile
```

-	Layers:
	-	`sha256:a4fae75dcb8b98151873f6aed4c918d1d169bb2c6f976d49a13b3ab27a993b44`  
		Last Modified: Sat, 16 Nov 2024 02:38:56 GMT  
		Size: 4.0 MB (4037988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:558f4b3ac537ebcea340f5bd3a0be51fcee9e6242ef292ec7c21930cca99bde7`  
		Last Modified: Sat, 16 Nov 2024 02:38:55 GMT  
		Size: 31.7 KB (31703 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3769fd95d2f32b594d5feaf9a7e88fe05acbc0d9a7e299052c2dfc2a95782883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156732893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5c24b812a07080e95f044d3af95181bb9cc3c764615ff34c29369157076d81`
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
COPY dir:d2a8722a4dd7b1d0cd44e2eb99d2153a3f0587d33eb0a412159a6143bce9563e in / 
# Mon, 04 Nov 2024 20:52:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 04 Nov 2024 20:52:12 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 20:52:12 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL "build-date"="2024-11-14T14:59:28" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Mon, 04 Nov 2024 20:52:12 GMT
RUN /bin/sh
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
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.4 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 04 Nov 2024 20:52:12 GMT
ARG MARIADB_VERSION=11.4.4
# Mon, 04 Nov 2024 20:52:12 GMT
ENV MARIADB_VERSION=11.4.4
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: MARIADB_VERSION=11.4.4
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: MARIADB_VERSION=11.4.4
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
	-	`sha256:ba55045592163ae9fdfe176806916bcad280c11028539767400b680f8aa54bf4`  
		Last Modified: Fri, 15 Nov 2024 00:13:46 GMT  
		Size: 44.3 MB (44342558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851b2c1a1842b755bf70a503867ac6650b8362aaa07d4e3596f8ec456a377ae7`  
		Last Modified: Fri, 15 Nov 2024 00:13:45 GMT  
		Size: 63.6 KB (63570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37956f5464f71073c4c5abf1aeeb2960d6a699ac72d6dc537ec0c09c66dec374`  
		Last Modified: Sat, 16 Nov 2024 02:24:04 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cac62dab673a4f53d8134ff19b79c212a97baf3159590266635f20ae5d3d764`  
		Last Modified: Sat, 16 Nov 2024 02:24:04 GMT  
		Size: 904.3 KB (904289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8bf3d56d54bd782fe995f5638db9912dc86047a9fc68c19dfd1be82fc5989c`  
		Last Modified: Sat, 16 Nov 2024 02:27:43 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d158f739d943a54fa38fb0597758bc26490d4b01ca3c0ef326012298340894b4`  
		Last Modified: Sat, 16 Nov 2024 02:27:43 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5336910d274ad6e9deb5a8c8f9a6265778ff092e369c747154093977f480a842`  
		Last Modified: Sat, 16 Nov 2024 02:27:46 GMT  
		Size: 111.4 MB (111408382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a92d5a223ec71038ff6e60d4cfe5b8595e59296d9a2bce0879ba80e8f010aef`  
		Last Modified: Sat, 16 Nov 2024 02:27:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ddd675b97ed85ce18a5089e8070350833bfe1f63fa002bcc277599aa6163d6`  
		Last Modified: Sat, 16 Nov 2024 02:27:44 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1764b28f7667684d71d1fecce254b27e8ff46b88b42bdb7347ed80ca9174f7`  
		Last Modified: Sat, 16 Nov 2024 02:27:44 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:6142001cd60d5625cbe1b51aeccc23bbc1c94ef171c56f5f2316c369ec2f9b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4070785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5042791cf3f27eb55a7711775909dd5b881bae45bcba1210d8f0ba48baa39e`

```dockerfile
```

-	Layers:
	-	`sha256:32a0ee895b1a21e1d667f2beef0fdef2390e09ef1ac3d921a3e181cfed69bb82`  
		Last Modified: Sat, 16 Nov 2024 02:27:43 GMT  
		Size: 4.0 MB (4039193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cdcf26bad687d5087c4e77b3c4a5e7dfdc43056aa0764aac9968bd8f2132077`  
		Last Modified: Sat, 16 Nov 2024 02:27:42 GMT  
		Size: 31.6 KB (31592 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:975e8a79af4ca6ffe5abef459da274ef2fbf47a53c1304e48422f9602ca9586c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (144951593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760c6b348e1a2d8bbf9d39bfb3f00730ed1593b9b0dd0c75b3f37b8a242c6366`
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
COPY dir:958a24c6c96abf98339b55dff343fa51b290f7250f0291ec25f8287a18a93135 in / 
# Mon, 04 Nov 2024 20:52:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 04 Nov 2024 20:52:12 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 20:52:12 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL "build-date"="2024-11-14T14:13:44" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Mon, 04 Nov 2024 20:52:12 GMT
RUN /bin/sh
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
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.4 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 04 Nov 2024 20:52:12 GMT
ARG MARIADB_VERSION=11.4.4
# Mon, 04 Nov 2024 20:52:12 GMT
ENV MARIADB_VERSION=11.4.4
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: MARIADB_VERSION=11.4.4
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: MARIADB_VERSION=11.4.4
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
	-	`sha256:c21c4caf6c15f91610a555c667b57afdcc48e2d0f5434c0077162a874a743541`  
		Last Modified: Fri, 15 Nov 2024 00:13:39 GMT  
		Size: 38.0 MB (37999212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768fe5fae363fdc94ec36a5d72b496812ff5d0a7c20395b415c2f7d39bbca5a2`  
		Last Modified: Fri, 15 Nov 2024 00:13:37 GMT  
		Size: 63.5 KB (63544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b147e325133497c837a1d56a305a0463fc1536c7fe5eb00fee05437da7377c55`  
		Last Modified: Sat, 16 Nov 2024 02:20:34 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407893a4d118c01d4b18970feeb0df5dc0f6e36ebba8196a5dc992f649abfe4c`  
		Last Modified: Sat, 16 Nov 2024 02:20:34 GMT  
		Size: 948.1 KB (948108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17a6c4047cd78b25f0e493d29de090fc529c098c228b0aa169b1e1a5ff444e7`  
		Last Modified: Sat, 16 Nov 2024 02:23:36 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c39d008f886b45b06618ab01094878fa0d4e91c945343d19a7b8fbb831eb234`  
		Last Modified: Sat, 16 Nov 2024 02:23:36 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cafd5b14f2f9fc2c41a306b281ce0798de24e9a63fbe490a2882249f1aab03`  
		Last Modified: Sat, 16 Nov 2024 02:23:39 GMT  
		Size: 105.9 MB (105926642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220ca9347914653334a557ac54c85b42acfef253f2bfb7847b6fb11dbd6a6d42`  
		Last Modified: Sat, 16 Nov 2024 02:23:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af754288579ce939ed59b971c8b9a22ded2f417cf24c0724dc77a6bd9529883`  
		Last Modified: Sat, 16 Nov 2024 02:23:37 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6cbd72f283bb40495c6b135d7fa35839562908c1b88710879131dca1a0ece7`  
		Last Modified: Sat, 16 Nov 2024 02:23:37 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:cff3e4b0c1273600d1f24fc844ab5ad21ba5219e8d43e28994236d8df49f0a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4070714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812bd6f48ec82556924fa3c04f761e88423e766426f23ad1301cbe911e4b834b`

```dockerfile
```

-	Layers:
	-	`sha256:c8b3574efb16b3e2ec9cc8428c2cb41a9626f6fb1fbc6aa3ad6e3a322e35ac64`  
		Last Modified: Sat, 16 Nov 2024 02:23:36 GMT  
		Size: 4.0 MB (4039178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:202107f67f20afac13daed3efa6b151d441f1b5139db4256c6c1ef24e37ea769`  
		Last Modified: Sat, 16 Nov 2024 02:23:36 GMT  
		Size: 31.5 KB (31536 bytes)  
		MIME: application/vnd.in-toto+json
