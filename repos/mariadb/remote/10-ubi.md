## `mariadb:10-ubi`

```console
$ docker pull mariadb@sha256:1f63fc0a93439de65026b6388f06d9915f326896cf952475ee285a8fc8fb42e6
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
$ docker pull mariadb@sha256:6c3b891b3c2ecb2ae42be305afb186cc40b8a3742716f7168c87786ebd445a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146528670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabe752f62a53180a820ebe73b1c7e197ad03c1d9ef6733e48f0f82669f615af`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
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
COPY dir:9782e2e1b0ca599e0a33d178720d08213ae97157f753b7e5bae27ac0755f7280 in / 
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL "build-date"="2025-05-14T10:35:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:a080cada37e9f7003fcfc13eb6b0d19a9d6c4bfa9b3a9cb9ef46b184cfa60e43`  
		Last Modified: Wed, 14 May 2025 14:33:02 GMT  
		Size: 39.6 MB (39645097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f79c9ecd51b71c6f1b43236d82a3afe2f74f205b814946faf7aaa60f2a86aa`  
		Last Modified: Wed, 14 May 2025 23:48:54 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31752553b6286a745384381ced7787cc84963634f2c971d6f4ab962153ce425`  
		Last Modified: Wed, 14 May 2025 23:48:54 GMT  
		Size: 983.5 KB (983469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23dc267620888bdcff14c24a8c51086dddffccdf6e12caf1224534b5347aaa96`  
		Last Modified: Wed, 14 May 2025 23:48:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998ed2ef5d414dafac0069fb3c8f6388b22d9aad8fe05073e7849d5b104b4827`  
		Last Modified: Wed, 14 May 2025 23:48:54 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daebb683d99c6a924ca86a41d16675f9c2598bf7c371895b139b12c882c7fb7`  
		Last Modified: Wed, 14 May 2025 23:48:57 GMT  
		Size: 105.9 MB (105886068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8970492e3d0c707c69993b37c273600db4f566ae0527a78904c5c0a21058806`  
		Last Modified: Wed, 14 May 2025 23:48:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682b30f9a5547c864c6ab5c91fc0f5538deed6bec0b40b51b7d01223c3553de6`  
		Last Modified: Wed, 14 May 2025 23:48:55 GMT  
		Size: 4.0 KB (4018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c60044ef64bdeb67be4b1c0fabf4c28df7949cf6f0aca5deb8b585ac41d76e`  
		Last Modified: Wed, 14 May 2025 23:48:55 GMT  
		Size: 8.4 KB (8365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:c75a8de1aaea623dae279103f9b9dc9bca7157a0e2b623beaa6652ad2ad0a7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96a6195f978880c582ed530bc52454b47247c3da82b4ff53f858ef5f109cb16`

```dockerfile
```

-	Layers:
	-	`sha256:70875798a64b5a56528ce51edf5c8d0a0d758dbdf17e2cb295ceec15435aaf12`  
		Last Modified: Wed, 14 May 2025 23:48:54 GMT  
		Size: 4.1 MB (4134833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b9de06a1dfdc284062f15df44c27b16cfeb99dce64a4f2d6d216e9ac7dfeda2`  
		Last Modified: Wed, 14 May 2025 23:48:54 GMT  
		Size: 30.2 KB (30193 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:000b0ec902e96497e04c941449c3ae01fd68576e90e11bf402cb973526b89d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158067702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3621b032c95564a39651dfb64000e4ae80516f3ab0b4caf78eb976681460e9f4`
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
COPY dir:322b1eba0279fa9048b9b4a366e8c52ac2af46fb06d006174f85e5f3b1ca4d6a in / 
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 21:06:18 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL "build-date"="2025-05-13T04:46:37" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7575d7eb45eb7f545fef31ba067dfe3d8e52c4eb" "release"="1747111267"
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
	-	`sha256:3a51516451292e212d18ae92028ed74f1d747fc2bc7752aa8c608a2cc7d626cc`  
		Last Modified: Tue, 13 May 2025 05:30:51 GMT  
		Size: 37.9 MB (37887912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3b3d9dc7f85d3c777eda6d9a7ce5593f234a92e7a33bfeb6526fc3377b1a8d`  
		Last Modified: Tue, 13 May 2025 20:10:46 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1eb2113225e33ac868d95fc4c7ebd33ffed52e577c0d3dcbdd926abbf6a496f`  
		Last Modified: Tue, 13 May 2025 20:10:46 GMT  
		Size: 913.8 KB (913805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2baf5e96c0691525f1663646cc4650d6406fec9e0fe00a43e4031eafeb4a62`  
		Last Modified: Tue, 13 May 2025 20:13:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b891179622d95d3fbe30978c7e0533c86243214ba3febf74a0e5988f210212e4`  
		Last Modified: Tue, 13 May 2025 20:13:54 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9135262af15b40209bab0b6851ad87b09ab75bb9ce3673bea42f622fc64d3049`  
		Last Modified: Tue, 13 May 2025 20:13:57 GMT  
		Size: 119.3 MB (119251951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd161143013265dd315d5f674d1fd4c2a45cde64ca38abbf3e2f11fef1e03ec`  
		Last Modified: Tue, 13 May 2025 20:13:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f48e48768a248dc45bbabfec947431e49e63424da184d3ff242260ae602554`  
		Last Modified: Tue, 13 May 2025 20:13:55 GMT  
		Size: 4.0 KB (4018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e519d090cbdfcf11a7751627eb2e081cfef805d4fa7e50752839fa8ecfcb0e8d`  
		Last Modified: Tue, 13 May 2025 20:13:55 GMT  
		Size: 8.4 KB (8366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:95cf59180382929615ead6c9173ed6304aa8c1ffe1265b8141e716fb368f0197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:117603638fbae543226abf6f1784107d63d7a07bc6740ce82d12e50bc4a6c34c`

```dockerfile
```

-	Layers:
	-	`sha256:528cdbb06d4145ef86f480fd593549abdd365a72b22f213ef15cdaa6bf628523`  
		Last Modified: Tue, 13 May 2025 20:13:55 GMT  
		Size: 4.5 MB (4490564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28aef4232f7c8c23e0477824e82ad7f07d26e85da06df43379bdd4e2eb6304c5`  
		Last Modified: Tue, 13 May 2025 20:13:54 GMT  
		Size: 30.4 KB (30362 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9c014b82bbe8bca06ec02ab13915ba073cb5c728bb95ca4a7f5467a95a4a93c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175459385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89042d07658708e4f152e0b145345c11b48ca71d1b6de8fdcf70056587a84aa9`
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
COPY dir:1085018760758e09e42995e4c88ff4dd151e77c58d5ef6b3654b47a7c40a27eb in / 
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 21:06:18 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL "build-date"="2025-05-13T04:46:00" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="7575d7eb45eb7f545fef31ba067dfe3d8e52c4eb" "release"="1747111267"
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
	-	`sha256:1e82e3f37bad53b3e574e762d5a9cf832ead379f56b78ecc079225e906404e68`  
		Last Modified: Tue, 13 May 2025 06:13:41 GMT  
		Size: 44.1 MB (44122666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103861394b96108a181eb55953f96cd254cc968b68712e5140c8c2f4d86f1f7c`  
		Last Modified: Tue, 13 May 2025 20:31:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa632b5a5ad17b7a8aa2d40c94e6fd0e9cc15b44abc52c4cd4ac44a07cf8b9e`  
		Last Modified: Tue, 13 May 2025 20:31:56 GMT  
		Size: 904.3 KB (904311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ea7d9287e25268c011dd484379250c7a57989d4ef8e1d4e34a607dc27ad31b`  
		Last Modified: Tue, 13 May 2025 20:38:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fd74f0ee109077aadfeb9d4bc8b21c4cdcba7e0f3b6c64128669f171499e7c`  
		Last Modified: Tue, 13 May 2025 20:38:17 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13af19f42b53e56ba24413a1f996bac2dd974c5bcd5b3b52712495c15a367616`  
		Last Modified: Tue, 13 May 2025 20:38:21 GMT  
		Size: 130.4 MB (130418375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6c420681a50cc19f3bc9f67ca193a86761f223effd49b18b05f6ac80446e31`  
		Last Modified: Tue, 13 May 2025 20:38:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dbe356f1f7f9174f6eccc8d7cbe7e536ab7db5ffcc086790d56ef768f7e1f1`  
		Last Modified: Tue, 13 May 2025 20:38:18 GMT  
		Size: 4.0 KB (4019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e65753631c9098b7f3871b71976a5ae1b24ddb7dfe48670971b5fdcdd579a0b`  
		Last Modified: Tue, 13 May 2025 20:38:19 GMT  
		Size: 8.4 KB (8362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:8ea9d4f443fa73d81843f13f154a77573ab332595b725ffed6f1d929ca12cb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b904a80186352d3cbd9593bc972beefa39ce9905a8bbc4d749e35048e223dc58`

```dockerfile
```

-	Layers:
	-	`sha256:f6487be62e7e9deb7a2c3347818650fef97f0470680e9e423a71d57ed134d7af`  
		Last Modified: Tue, 13 May 2025 20:38:17 GMT  
		Size: 4.5 MB (4491791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93779bb7e8b50c5dd17419fd200b956877976d4add81c5f14ad3825987a26b56`  
		Last Modified: Tue, 13 May 2025 20:38:17 GMT  
		Size: 30.3 KB (30251 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:5e6feda86268d387137c27e65e1b2e44c3745ac159ba9156af2db4b73a4c72f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145224208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cec5ed1a974c84fd6ce07955c00df8e272e6a98f6cf94e24d7f5f60c6eec4c`
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
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
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
COPY dir:342a15ffc31d680c780a31bc68e55ce86efa55579df99a39d0cad8e323a0e4f0 in / 
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 05 Feb 2025 21:06:18 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2025 21:06:18 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 05 Feb 2025 21:06:18 GMT
LABEL "build-date"="2025-05-14T10:42:34" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="f2f252e0ac953b9e80eaebfc08ec086edac81945" "release"="1747218906"
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
	-	`sha256:2bdd6e8a1a405237e41cdf28c04feb04cf2890537bf6109911a282b7ce3ac2e0`  
		Last Modified: Wed, 14 May 2025 18:10:27 GMT  
		Size: 37.8 MB (37799622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caf8defa3bfa86c217ebd76ec3b9868d67b48a52259d74a1d01c70c996aeec5`  
		Last Modified: Wed, 14 May 2025 23:56:15 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d56819a156f65ef1c6abc9d2b9e78c1c697cb111241d0a111a84e53e5eaf80f`  
		Last Modified: Wed, 14 May 2025 23:56:15 GMT  
		Size: 948.1 KB (948114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc9660112a7922eb46d72e876473a549c62c339022deff00f7d47ecf48b5084`  
		Last Modified: Wed, 14 May 2025 23:59:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246b8875fc603401b6cfd4d90d2c9fe9654a46b41ce339eea8fcc95ad197e79d`  
		Last Modified: Thu, 15 May 2025 00:00:00 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bc034922c8bcbd66df5207c3a6a984d3ad55849c9c0bd1d4f32fd4982c6107`  
		Last Modified: Thu, 15 May 2025 00:00:02 GMT  
		Size: 106.5 MB (106462439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9219d7c62c982bfb6b406a75c456e1af76e1fed40ede5056ea96ff411ff7e548`  
		Last Modified: Wed, 14 May 2025 23:59:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76ae6bdd283aac84cfb5ab0c34f998aea4dc007be11f53ee2a81b498dbe5af4`  
		Last Modified: Thu, 15 May 2025 00:00:00 GMT  
		Size: 4.0 KB (4018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb65a53b13e868d24d80f9fa698501f7a7579af3d5fb7d0a1c21d0838aa3a92`  
		Last Modified: Thu, 15 May 2025 00:00:00 GMT  
		Size: 8.4 KB (8363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:42218ff548f5bd74456839b25174428774b787b186a98dcbca221eb015b059ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4166282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e3f5587a45563b61d2ee106c54cce970a86ed43132b2cdcdab833eb64d3ad5`

```dockerfile
```

-	Layers:
	-	`sha256:e70c29fb748ddaeb5680440f619df09046a87d6f918a70e696381abddd1cd66a`  
		Last Modified: Wed, 14 May 2025 23:59:59 GMT  
		Size: 4.1 MB (4136087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85e3668f90126bdd0016abaaccef9c0392a7be2513707180dee7bd92ab7b2837`  
		Last Modified: Thu, 15 May 2025 00:00:00 GMT  
		Size: 30.2 KB (30195 bytes)  
		MIME: application/vnd.in-toto+json
