## `mariadb:10-ubi`

```console
$ docker pull mariadb@sha256:0cd87a980830e1a49ec50de4f60b090ef612187154047c2f8c4706df6d117500
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
$ docker pull mariadb@sha256:90ed8c242c13b76b9fe241abe970908aa82c3fc910b5f555333e14a6818da46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154151293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dbdbeffaaa3724b40d57cbbee1c83e50d2c026757e7f49f90528e7aa9af661`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.openshift.expose-services=""
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 10 Aug 2025 22:04:52 GMT
ENV container oci
# Sun, 10 Aug 2025 22:04:52 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 10 Aug 2025 22:04:52 GMT
CMD ["/bin/bash"]
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Sun, 10 Aug 2025 22:04:52 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
ENV GOSU_VERSION=1.17
# Sun, 10 Aug 2025 22:04:52 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.14 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.14 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 10 Aug 2025 22:04:52 GMT
ARG MARIADB_VERSION=10.11.14
# Sun, 10 Aug 2025 22:04:52 GMT
ENV MARIADB_VERSION=10.11.14
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=10.11.14
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
VOLUME [/var/lib/mysql]
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=10.11.14
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 22:04:52 GMT
USER mysql
# Sun, 10 Aug 2025 22:04:52 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 10 Aug 2025 22:04:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b34bc1d80111fe14d5d3b465b82b7d5dc805ed7167e4159dac3b03cfcf9624c`  
		Last Modified: Thu, 21 Aug 2025 18:57:00 GMT  
		Size: 4.8 KB (4770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b320ebcbe99b2314461bf72bc68e8739c3b20bbff599d1adeb9951b138a21f8`  
		Last Modified: Thu, 21 Aug 2025 19:19:44 GMT  
		Size: 2.0 MB (2003495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2988c6a557b2afbda2d6585ee7b08ff708d4c062fe674faa51a7d74d558df3`  
		Last Modified: Thu, 21 Aug 2025 22:08:57 GMT  
		Size: 7.0 MB (7042924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bb1378e118a9accf5fd9a94035a09fb11f0010a28511069a7cb3696fab15e8`  
		Last Modified: Thu, 21 Aug 2025 19:19:49 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a51a11c4843b09381e32a35d105c566607c271fbcb5341d8a33c00baebd695`  
		Last Modified: Thu, 21 Aug 2025 19:19:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b082765988b25ee15c78836503ce4ff1d56b890d470f8d4b8b138bf43f1d45f3`  
		Last Modified: Thu, 21 Aug 2025 22:09:02 GMT  
		Size: 105.4 MB (105439648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac89e4c79aa56b63de87d8b28e36554072b44090de45de08046a1d028a83003`  
		Last Modified: Thu, 21 Aug 2025 19:19:55 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306d91b9e48f7de3e786e370405fb3ac1ccb4748ff567782a3cc2f0ee8a18e58`  
		Last Modified: Thu, 21 Aug 2025 19:19:59 GMT  
		Size: 4.0 KB (4019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab950ef67fae2c633cb7e33e8a7f59c835734631275ee47eca01f533a7b212a`  
		Last Modified: Thu, 21 Aug 2025 19:20:02 GMT  
		Size: 8.4 KB (8368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:326bf171739fa8809799e5179f938b1ccdc6de7e9f84cbed2f9c27363007f810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e62b0f6ff23589db4348bb3cb7fe55561509cc643ffc11ba8104811d856746c`

```dockerfile
```

-	Layers:
	-	`sha256:648690f8abff7c8aef9314f0923feb7f98d1fb35099f84cd7b3fb48775744104`  
		Last Modified: Thu, 21 Aug 2025 21:35:33 GMT  
		Size: 4.1 MB (4118232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:677120866560b9b31e3f2a395017485e14cb3dad8b8fc620b6e1286f546e7c00`  
		Last Modified: Thu, 21 Aug 2025 21:35:34 GMT  
		Size: 33.8 KB (33762 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5cf9d84b34285206e88131aaa592610f38d899244f5355b74e1f1e4b2df76cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149829250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60cbef18de360bd9e658ab5dafa820fddf39151b34afdd6b79b4f5a5d10fa47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.openshift.expose-services=""
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 10 Aug 2025 22:04:52 GMT
ENV container oci
# Sun, 10 Aug 2025 22:04:52 GMT
COPY dir:f91aecd64a5df0b73e2b5740ae90f4bb03c2e87890175a65862ca830f6caced5 in / 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 10 Aug 2025 22:04:52 GMT
CMD ["/bin/bash"]
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL "build-date"="2025-08-20T13:14:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Sun, 10 Aug 2025 22:04:52 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
ENV GOSU_VERSION=1.17
# Sun, 10 Aug 2025 22:04:52 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.14 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.14 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 10 Aug 2025 22:04:52 GMT
ARG MARIADB_VERSION=10.11.14
# Sun, 10 Aug 2025 22:04:52 GMT
ENV MARIADB_VERSION=10.11.14
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=10.11.14
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
VOLUME [/var/lib/mysql]
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=10.11.14
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 22:04:52 GMT
USER mysql
# Sun, 10 Aug 2025 22:04:52 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 10 Aug 2025 22:04:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405fc63d30a0cf601ac33dc7e97f20169af4972eb484a059a5ea8a12b5ce061e`  
		Last Modified: Thu, 21 Aug 2025 19:34:59 GMT  
		Size: 4.8 KB (4770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0207fd6583eb06abaf1419f915577051f29e7d03cd4145af9d71f82e322d63d`  
		Last Modified: Thu, 21 Aug 2025 19:35:01 GMT  
		Size: 2.0 MB (1997197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016b651ba720ec291bf53918b0f2a45b807844462bdd556626ac8b9ef868653d`  
		Last Modified: Thu, 21 Aug 2025 19:35:01 GMT  
		Size: 6.1 MB (6105116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b062ff7dd6b07e7354fa7ab12ae4bf472a9f95a04fbb3e59041dbeb49666d48`  
		Last Modified: Thu, 21 Aug 2025 19:37:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000ac2ef8ee74eb19c043c5d992180f3e52eb493bc35531752a1dcef621a4fa2`  
		Last Modified: Thu, 21 Aug 2025 19:37:13 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239ea9106851340b622643331c665d94d3ac76c3d8767cee82ec4a5a98831e10`  
		Last Modified: Thu, 21 Aug 2025 19:37:27 GMT  
		Size: 103.8 MB (103849420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b692781465ce6759aab9b81fdfd9f3ff7ca8a15d0f7e6e5776f50a7ddd931904`  
		Last Modified: Thu, 21 Aug 2025 19:37:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacb063875de349a36f833d04f94eb78b3915ab2dd52d51bca5649e86ad07569`  
		Last Modified: Thu, 21 Aug 2025 19:37:16 GMT  
		Size: 4.0 KB (4019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e889d265f6dd566c2711040657681373048f621ff1591627575b01cafdc5ae`  
		Last Modified: Thu, 21 Aug 2025 19:37:14 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:8af040a0731c04f7da173dc283322a65df838820e2db6e64b571ec1f677e4608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e782936d09633b246ce6cd1a1d2d8fc6a891450b9e52209e86738be3252ad0`

```dockerfile
```

-	Layers:
	-	`sha256:3d7d0016ad05b56d66d2f87ca921c9dbbc9075baeb346deac5be416727ed167c`  
		Last Modified: Thu, 21 Aug 2025 21:35:39 GMT  
		Size: 4.1 MB (4118274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cbeb29046e051e84bc705f06144fea38222f0d2a3024cc293381ecb9f23e7e4`  
		Last Modified: Thu, 21 Aug 2025 21:35:40 GMT  
		Size: 33.9 KB (33945 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:91c29d0628797a08154d0b18de6730ab8188b7bbedc2fc2b3e4ca45b384c0b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163676166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8550b5e211dbad027b536168fee095dc376108ba20e4048861149b7e69da9da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.openshift.expose-services=""
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 10 Aug 2025 22:04:52 GMT
ENV container oci
# Sun, 10 Aug 2025 22:04:52 GMT
COPY dir:d2207f84596636cf1f42082a4111b6c38656ec970ae8b2e1ce2cacd7d29f1510 in / 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 10 Aug 2025 22:04:52 GMT
CMD ["/bin/bash"]
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL "build-date"="2025-08-20T13:11:42" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Sun, 10 Aug 2025 22:04:52 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
ENV GOSU_VERSION=1.17
# Sun, 10 Aug 2025 22:04:52 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.14 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.14 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 10 Aug 2025 22:04:52 GMT
ARG MARIADB_VERSION=10.11.14
# Sun, 10 Aug 2025 22:04:52 GMT
ENV MARIADB_VERSION=10.11.14
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=10.11.14
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
VOLUME [/var/lib/mysql]
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=10.11.14
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 22:04:52 GMT
USER mysql
# Sun, 10 Aug 2025 22:04:52 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 10 Aug 2025 22:04:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:ebd7c9ee3cc0108f33ad80f84c3da96a78c10cc76b3dfe38b2b8ab879a83a307`  
		Last Modified: Wed, 20 Aug 2025 18:13:19 GMT  
		Size: 44.1 MB (44057494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ab0339a62212469391e8fcb5883cf9c96859b56f720a650a8278286b5a2bca`  
		Last Modified: Thu, 21 Aug 2025 19:22:46 GMT  
		Size: 4.8 KB (4770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3578090037abd18b7884160fc2c7e48225b3bad9d39c4a79cad38d5c76e26746`  
		Last Modified: Thu, 21 Aug 2025 19:22:47 GMT  
		Size: 2.0 MB (1994155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377b2324eca093eb84fbb4c1bad2daaf206c86fcb6f04e92592ff311189a15c9`  
		Last Modified: Thu, 21 Aug 2025 19:22:47 GMT  
		Size: 6.1 MB (6069585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc90396eb740846c9eb7121c6d8f9e084397169303b581b96455f9354fe9bba`  
		Last Modified: Thu, 21 Aug 2025 19:26:09 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e2eda08479e6fe3e27fbeaa0bdaec3ac09a6905fe7fdc625aa391c95035227`  
		Last Modified: Thu, 21 Aug 2025 19:26:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ce913c059b1fed1d56c26b53ea2503730afe71f3f5d9cc7c43845571bec0cc`  
		Last Modified: Thu, 21 Aug 2025 19:26:22 GMT  
		Size: 111.5 MB (111536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54684b548a48e0073454be46f5eda01fe9873e3e20172638a7a36ad85bdd0f9`  
		Last Modified: Thu, 21 Aug 2025 19:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8142ee6f6354b523a90e4e76d678e5176403dcb3c2c6c9d10ba91db2671ce9c`  
		Last Modified: Thu, 21 Aug 2025 19:26:10 GMT  
		Size: 4.0 KB (4015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a501b6fe5c65c113e7d2403f34de6ec75a74af6b3778a4a909970c9c2d3bf76`  
		Last Modified: Thu, 21 Aug 2025 19:26:12 GMT  
		Size: 8.4 KB (8365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:d3850a5e789fedde65a39939b9b14defe011487d59f608afbfbed2692a6c4a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4155982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfe837c2697fb2f196521257fd4beda5ed13d5d085e10c27d3a90f8ac1cfe75`

```dockerfile
```

-	Layers:
	-	`sha256:bd85e95388365ea5b2bd3aea63431e4792351102b2a331204365aa7d58dcc178`  
		Last Modified: Thu, 21 Aug 2025 21:35:44 GMT  
		Size: 4.1 MB (4122161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090a8bb3a8abb9b756d87d94f6f214c5d4de30d1a074f4a0b48330ccc9df89d0`  
		Last Modified: Thu, 21 Aug 2025 21:35:45 GMT  
		Size: 33.8 KB (33821 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:14b1152ee5ac3dbfac15729d0d12caefd801f62b3a6e9c4088d8900afc76c742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151933292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499d36ecc7df3c13521ada0ab5aff22ca3e8d533a732c94ac4e7051bcf10480e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.openshift.expose-services=""
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 10 Aug 2025 22:04:52 GMT
ENV container oci
# Sun, 10 Aug 2025 22:04:52 GMT
COPY dir:50d215ebed2bd8f3ebc927c36f9221810f1ee237dd8666d613479d55333c24b0 in / 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 10 Aug 2025 22:04:52 GMT
CMD ["/bin/bash"]
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL "build-date"="2025-08-20T13:21:17" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Sun, 10 Aug 2025 22:04:52 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
ENV GOSU_VERSION=1.17
# Sun, 10 Aug 2025 22:04:52 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.14 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.14 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 10 Aug 2025 22:04:52 GMT
ARG MARIADB_VERSION=10.11.14
# Sun, 10 Aug 2025 22:04:52 GMT
ENV MARIADB_VERSION=10.11.14
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=10.11.14
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
VOLUME [/var/lib/mysql]
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=10.11.14
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 22:04:52 GMT
USER mysql
# Sun, 10 Aug 2025 22:04:52 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 10 Aug 2025 22:04:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:3f0282e908208d8e7c1713535fd66f131da1a731129cef1ea3f76c45ef5710cb`  
		Last Modified: Wed, 20 Aug 2025 18:13:17 GMT  
		Size: 37.8 MB (37760918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7a7e68b5341da44b8c40fb1b75804c3182780d7a38870b1de1e994970ab7cd`  
		Last Modified: Thu, 21 Aug 2025 19:59:04 GMT  
		Size: 4.8 KB (4770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf999c0ae982281487553148ef65240526a638882c6f6b2418e59740e69e15f0`  
		Last Modified: Thu, 21 Aug 2025 19:59:04 GMT  
		Size: 2.0 MB (2010429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9919c9f469f391b773c2e69c4c19ff1a921976d3116d6cee333896727a49af20`  
		Last Modified: Thu, 21 Aug 2025 19:59:04 GMT  
		Size: 6.1 MB (6084937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df07d9e360890b641fea26d52eeabb31229178218fe329efd253c106bf344238`  
		Last Modified: Thu, 21 Aug 2025 20:07:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06e86dec9fcc4a5f230b5ec32efdd7ff42c06388587ecbd63e0731938ee3334`  
		Last Modified: Thu, 21 Aug 2025 20:07:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831e525c380ec60beb83451adeb717bf597f6fd2a58cdfe10a1ce9b4939ea63b`  
		Last Modified: Thu, 21 Aug 2025 20:07:18 GMT  
		Size: 106.1 MB (106059060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6396ead516f47ac98a2051e754e7caa45779f085c6fc1afb7e6ad5a0e92a54e7`  
		Last Modified: Thu, 21 Aug 2025 20:07:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7f81b47c3c8848702261792c31d218df2354853ef8c9cae7c4f68586ac4441`  
		Last Modified: Thu, 21 Aug 2025 20:07:05 GMT  
		Size: 4.0 KB (4020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9d7f082f5e84887bbe0e4180c7d8a6232278ab380075a8756d0715ba46c2b4`  
		Last Modified: Thu, 21 Aug 2025 20:07:05 GMT  
		Size: 8.4 KB (8368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:2595f532956d94b6891b04ddf4a89d6ac4fa2555a6f068012ff1f341e5b61669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4155909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6337b14c1d41953aaba7d6bc0c1abe4ee5416cc830106501add71ba3f55212`

```dockerfile
```

-	Layers:
	-	`sha256:29eab4442c4d609e28a3b88355744ba7505459cdebc9715a78b372a72b9fdcb2`  
		Last Modified: Thu, 21 Aug 2025 21:35:50 GMT  
		Size: 4.1 MB (4122146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c41c502376f8ef1f53799937aeae8b990438a1fd5d3ec72ab97fdcd1c58191a4`  
		Last Modified: Thu, 21 Aug 2025 21:35:51 GMT  
		Size: 33.8 KB (33763 bytes)  
		MIME: application/vnd.in-toto+json
