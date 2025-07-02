## `mariadb:11-ubi`

```console
$ docker pull mariadb@sha256:ce3494fdb2392d300f397b10c244c3c14841a1b8fe0e93f0ee5de23282b233dc
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
$ docker pull mariadb@sha256:29f67a2f20376933f7df76040cc5a99df28201faa9cf6e031674eda2efef74dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147610384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:564e469cf87698326586ec61c4a823e1df237c7302d0de0a3ee150a9663b72c0`
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
COPY dir:dca6230157d1db8824aac8b8e02a58f86449d038270aad6f0997ce65db8f8656 in /    
# Tue, 10 Jun 2025 21:48:21 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 21:48:21 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL "build-date"="2025-06-30T12:32:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
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
	-	`sha256:1ec5864c36114bbcd01f21fd199950f3730f43e1c94cc7b37c7bbf8bd446148d`  
		Last Modified: Mon, 30 Jun 2025 13:22:01 GMT  
		Size: 39.7 MB (39650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4edc13d9e9397cec6559050d4c5373fda634712b0381f20b7bbbcba4d881d10`  
		Last Modified: Wed, 02 Jul 2025 18:44:58 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bd49d387a3ca821f489d452739ff445d78af7898ca783224a37d8b2f963f9d`  
		Last Modified: Wed, 02 Jul 2025 18:44:58 GMT  
		Size: 983.5 KB (983466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567b9757c128d0ce37b55c4c9d4d605854650f49c815c12f7e9089d237cb59e9`  
		Last Modified: Wed, 02 Jul 2025 18:44:58 GMT  
		Size: 299.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcffce384f3e133e8dd5a2ae3591886c3c29ef82554b29ade7a167de0651830`  
		Last Modified: Wed, 02 Jul 2025 18:44:58 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e941dd578bba9f78eb0a51fc32d109913a97dd5c129ec6820a6032f577ede8`  
		Last Modified: Wed, 02 Jul 2025 18:45:10 GMT  
		Size: 107.0 MB (106962050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122be3298f600ea82d1d84e59c028ed636973714466fb3dd388724afbd0b0456`  
		Last Modified: Wed, 02 Jul 2025 18:44:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3852081e1537dbc0c87863c746c587ef2e71be7a4222f37dfe8665938b79ca74`  
		Last Modified: Wed, 02 Jul 2025 18:44:59 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e11b701ac1635cfa46389c0b6309d21c3f0a1717082e5d7a8de423eae8fb9`  
		Last Modified: Wed, 02 Jul 2025 18:44:59 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:c6b95e5ad87cf87e4db1af6ab045f7fd7f67c386c47fad0c6a5e8cef1df561f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeba327d4fcae654034b4e1e0a5c2af3475428744a77fd74c6f3d6cb799cf2a2`

```dockerfile
```

-	Layers:
	-	`sha256:9324348206d910c06d2edc4acb1dd65c88eddc8b9732092be1e82102739b1fe6`  
		Last Modified: Wed, 02 Jul 2025 21:36:22 GMT  
		Size: 4.1 MB (4139612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5467ced3338e279ef2cc490c8bdaef08cc9b19e7b0d2cba5ebce3ae11549fca5`  
		Last Modified: Wed, 02 Jul 2025 21:36:23 GMT  
		Size: 30.8 KB (30774 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:eb7040ed1a89aac28b5b7972185c06e190393e97728e6b1b392c967aada9a762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144218866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a78dbbf32359d98a0d812b2af491a6a4133ec85fd8b60c60d7149249412b79`
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
COPY dir:4a26990fc6a982252bab47a280479ef21eaa9fb0686b5810bf75da5fc5af7d4f in /    
# Tue, 10 Jun 2025 21:48:21 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 21:48:21 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json    
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL "build-date"="2025-06-30T12:36:52" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
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
	-	`sha256:ffb6dfc9a5fd85e709e0a3428084894621f9e001746e51a54875b13ff103e464`  
		Last Modified: Mon, 30 Jun 2025 14:20:11 GMT  
		Size: 37.9 MB (37864356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2db7d9f9323023d4713a39145d07e8b57caa4b7b313909791debd3da361511f`  
		Last Modified: Wed, 02 Jul 2025 19:02:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d187e9cdbb0753f5a675f0777deaabccf21086f0bdbf9c6eebbf7d3f7d8a92bc`  
		Last Modified: Wed, 02 Jul 2025 19:02:41 GMT  
		Size: 913.8 KB (913807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f9eda2334fac8a35c021144704f5e923f3eb3fd5d9ea72d3c71d77eb2a1bf0`  
		Last Modified: Wed, 02 Jul 2025 19:02:40 GMT  
		Size: 299.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603d3f935517c89bae12c532a91c54752fc93f4d78d3c327d25c105cf5dce54`  
		Last Modified: Wed, 02 Jul 2025 19:03:40 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e803508d52040904d65fe215f977c55a0c1b23f37ddb5166b6e949ff5d174990`  
		Last Modified: Wed, 02 Jul 2025 19:03:49 GMT  
		Size: 105.4 MB (105426656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c4baba623441e69d710f500c3aa04a6ff72cd090279c1bc4904ada6b27601a`  
		Last Modified: Wed, 02 Jul 2025 19:03:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4240f0085a7353e0f71527c786abca44066ddf58fd3862cbbd1b6a73ce7deda5`  
		Last Modified: Wed, 02 Jul 2025 19:03:40 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388e7c344e63b643999196ef3473e3bb1fb213249490dfd06c8532cdb0dc63fe`  
		Last Modified: Wed, 02 Jul 2025 19:03:40 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:c6977a3a03ca5a5aa523382b125e2604d8667727205b423a6ff9a4766f3f97d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8577a46d197ec031712e8504a6fea2f5f3a9c21f882c4c5fa859826a437ef6db`

```dockerfile
```

-	Layers:
	-	`sha256:1165d3f1f0d0b15c27d8502a070c988189eaac29cce50b6b9e03f6d5df405e48`  
		Last Modified: Wed, 02 Jul 2025 21:36:28 GMT  
		Size: 4.1 MB (4139678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75259c413b38b302d534c7b1ac59297290e7b45056f0095fa7b7a98a1505f68c`  
		Last Modified: Wed, 02 Jul 2025 21:36:29 GMT  
		Size: 31.0 KB (30965 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:00b0c6590f2c9303ed7add73c492a16d8ebccd8cfa279da05c6fd9cc9f671ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158248976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b6068b4be338721f2d6300cc57aad47dfa0d22ec473c445a5dd50917124a38`
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
COPY dir:6bd7d090c3df5ed04bb4f3de6886ab9cde9ba5683e238b0ef619fa4cb19ee2cd in /    
# Tue, 10 Jun 2025 21:48:21 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 21:48:21 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json    
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL "build-date"="2025-06-30T12:33:57" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
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
	-	`sha256:75a662397909644d17ddc808886bd00daef2f0268930ee1bde3570354249de79`  
		Last Modified: Mon, 30 Jun 2025 18:10:03 GMT  
		Size: 44.0 MB (44033425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01a54acedf3bde1800d34fe92eb558e2f2f1db093d28af33b8e9e3dc80cd8cb`  
		Last Modified: Wed, 02 Jul 2025 18:56:46 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727fe767e3ed009c85d075123bb6e50c5517961f9fb318c4a1748ea11bf66f90`  
		Last Modified: Wed, 02 Jul 2025 18:56:46 GMT  
		Size: 904.3 KB (904307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87951d691df0e264c12a27c7c3dbda74224f6d49372c66c390de0141e926a46`  
		Last Modified: Wed, 02 Jul 2025 18:56:46 GMT  
		Size: 299.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7e71e3285664ab0e6129426a518d138eb969bae3bbe8047a036bbf84c66c40`  
		Last Modified: Wed, 02 Jul 2025 18:58:50 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b92c1f78842475513d40d33fc77497e3cb343550c0ed93c345c1c53f823aa47`  
		Last Modified: Wed, 02 Jul 2025 18:58:58 GMT  
		Size: 113.3 MB (113297187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddd88fc2e82d76ee126d846509191f4e112eb4a47492954d5f7a17cd3bd5df1`  
		Last Modified: Wed, 02 Jul 2025 18:58:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f92b59dfc6fb184ba04a669981a4251da64d32354a88969cc3bb60c0bbc4677`  
		Last Modified: Wed, 02 Jul 2025 18:58:50 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb571eaa3ef310d2f0cd99145f1ef2e03166933b46c7215cd2c52e955d95def`  
		Last Modified: Wed, 02 Jul 2025 18:58:50 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:8c8f7a9c33ffb663d41d5defbf06fc517f9a151c5e12e7833aa12853a7bb58fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca42634f2e42a847a2bfb0cd5cbfd550b59676a83e950bfb5b0116d7c10d128`

```dockerfile
```

-	Layers:
	-	`sha256:461752adca30f74cf5a79d13ea31d25b65381b786298d0aef70938a98acbde50`  
		Last Modified: Wed, 02 Jul 2025 21:36:33 GMT  
		Size: 4.1 MB (4140869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cc320742bd13f4129026d93ea734fbe9292a532cfd4fd8683f70ca1d1619b5`  
		Last Modified: Wed, 02 Jul 2025 21:36:34 GMT  
		Size: 30.8 KB (30842 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:1ba305e548ffcb85ef69cbc5ecbafc75ff0d2554379bd0a9089fd6d5de2ea479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146412805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd048b3420889219c9430581e9efd93a16c6ee00ceda4ac83aa55f56b55b09f1`
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
COPY dir:1b67311835389ffe4ad4ead7fcea317b40582d80cd6ef953967b33a7d5cb65e5 in /    
# Tue, 10 Jun 2025 21:48:21 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 21:48:21 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json    
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL "build-date"="2025-06-30T12:38:11" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
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
	-	`sha256:2129d80cee89f438c6dbd429ffb54a5978b65e615ac7fd433ec00fe2bade0ebd`  
		Last Modified: Mon, 30 Jun 2025 18:10:12 GMT  
		Size: 37.8 MB (37768278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c514a477e97fd163c6ca8a6c98fe347743d9fd46c4338de389eca13888418ddf`  
		Last Modified: Wed, 02 Jul 2025 18:59:35 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5e62b35791565f4c6d1b63e2c3fc99e1400b0b6a317095fcd9872baff72846`  
		Last Modified: Wed, 02 Jul 2025 18:59:36 GMT  
		Size: 948.1 KB (948116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944ab724c10f843ebd0f596fa052b86c3b82ee3a081fea2f4b9baa7f112f4c61`  
		Last Modified: Wed, 02 Jul 2025 18:59:35 GMT  
		Size: 300.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e856ca63abd94d8e4b23246fe659aa2204549ac9d8d44934bd1d739d482f7ec1`  
		Last Modified: Wed, 02 Jul 2025 19:08:07 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca84fe01aba98e098526e523a172062b831f8ec952f7684a30638e330864f32`  
		Last Modified: Wed, 02 Jul 2025 19:08:16 GMT  
		Size: 107.7 MB (107682352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7363ccc35aaac5ed755bf55a0f1c929053183f79ca433e355db7348c74754e33`  
		Last Modified: Wed, 02 Jul 2025 19:08:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7672d8449969d331e3ade618dbc64c7df040f2644b179fe504e6282e7824540`  
		Last Modified: Wed, 02 Jul 2025 19:08:07 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46271380666d060f391d0f35586dc853bde0cf403821d7fc3e0078b7c4769991`  
		Last Modified: Wed, 02 Jul 2025 19:08:07 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:5e0528943cd25db397c4665cc98307d50f718f439d008a71edd3a7109647a2c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d334c7fc88ff863a64a547c98a03ce54fe3b6bfcd4c7a4a58e154900ad23bbcd`

```dockerfile
```

-	Layers:
	-	`sha256:eb70124ad644ad2761f23e55331531572306f8016ea852a9698ae8427427ab6a`  
		Last Modified: Wed, 02 Jul 2025 21:36:39 GMT  
		Size: 4.1 MB (4140842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbcde26f4c52d23a4e1db6de8dfa378adc4d4b62de0304241f5670ad60f6399d`  
		Last Modified: Wed, 02 Jul 2025 21:36:39 GMT  
		Size: 30.8 KB (30774 bytes)  
		MIME: application/vnd.in-toto+json
