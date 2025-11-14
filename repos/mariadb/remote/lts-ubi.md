## `mariadb:lts-ubi`

```console
$ docker pull mariadb@sha256:7c34a09adde5c83ee955a0754fa58a467539912955f51dedd5e8695102a21e02
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
$ docker pull mariadb@sha256:3d67f6fdcf025203197fa2545ef991bc46e436f54255eb1c9e1ee27b4f1a70b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167885797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d6efcd4532cb8d9cf6dfa0a590af217f1f66924013e5fe769b91ebcb28f509`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 12 Nov 2025 14:07:23 GMT
ENV container oci
# Wed, 12 Nov 2025 14:07:24 GMT
COPY dir:fd8f02dabe7ae9790ce0638d1f9e9f60d460b3580843d39cb4dee8e471c106cc in /      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 14:07:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:b446d7ec96d8598bdd079305b40e4e5a0c1e0d484658876cab87a4393ac52954 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:b446d7ec96d8598bdd079305b40e4e5a0c1e0d484658876cab87a4393ac52954 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:07:24 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="09400c6ea1039bbeb186633c5815980c077ced2a" "org.opencontainers.image.revision"="09400c6ea1039bbeb186633c5815980c077ced2a" "build-date"="2025-11-12T14:07:06Z" "release"="1762956380"org.opencontainers.image.revision=09400c6ea1039bbeb186633c5815980c077ced2a
# Fri, 14 Nov 2025 01:13:56 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Fri, 14 Nov 2025 01:13:58 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:14:01 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 01:14:01 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 01:14:01 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Fri, 14 Nov 2025 01:14:01 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Fri, 14 Nov 2025 01:14:01 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.4 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Fri, 14 Nov 2025 01:14:01 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Nov 2025 01:14:01 GMT
ARG MARIADB_VERSION=11.8.4
# Fri, 14 Nov 2025 01:14:01 GMT
ENV MARIADB_VERSION=11.8.4
# Fri, 14 Nov 2025 01:14:24 GMT
# ARGS: MARIADB_VERSION=11.8.4
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Fri, 14 Nov 2025 01:14:24 GMT
VOLUME [/var/lib/mysql]
# Fri, 14 Nov 2025 01:14:25 GMT
# ARGS: MARIADB_VERSION=11.8.4
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 01:14:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 14 Nov 2025 01:14:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 01:14:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 01:14:25 GMT
USER mysql
# Fri, 14 Nov 2025 01:14:25 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 14 Nov 2025 01:14:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:179ba4be1de0701de7b39988f2989858194723f60b56b12f8d9438358e471a73`  
		Last Modified: Wed, 12 Nov 2025 15:07:23 GMT  
		Size: 40.0 MB (40048414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacee34a58c84de47f95f70e5664a83b63702115a823f9391ee83ee52a55608b`  
		Last Modified: Fri, 14 Nov 2025 01:14:53 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b060eec1317805b32fa7dd9b2b5781a1f14447c241351a9db5a138f20add5f3`  
		Last Modified: Fri, 14 Nov 2025 01:14:53 GMT  
		Size: 2.0 MB (2010867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6df4844bd6a80a235ac6c929b9e835c86e037c0b24be1fcb5032dd39477553`  
		Last Modified: Fri, 14 Nov 2025 01:14:54 GMT  
		Size: 7.1 MB (7091201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb8b16cefc93f8dffeee184f10f97a636967016dc84307a00932f1845422ca2`  
		Last Modified: Fri, 14 Nov 2025 01:14:53 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7c1ad19a282631770a5beb3054e25b008ebb35aa62b2b2d924ac8251aff5e4`  
		Last Modified: Fri, 14 Nov 2025 01:14:53 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c910c80871242eee95cb2b52033cb0c99e8af3b2f7462c536b86c93e89f2b0b4`  
		Last Modified: Fri, 14 Nov 2025 01:15:04 GMT  
		Size: 118.7 MB (118717379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63cee36d6b65ae2072c8cd8aebb8ffc010df9c5a7e9da05982627d4bb3f720f`  
		Last Modified: Fri, 14 Nov 2025 01:14:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b1a86015d4eb2d3d516630709084de5361457473da81d7e5fbbd434405cbe1`  
		Last Modified: Fri, 14 Nov 2025 01:14:54 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84daabb9822f86b0c8a3986b5adbf77a7036b176e6d06086fedf444a4d2f9797`  
		Last Modified: Fri, 14 Nov 2025 01:14:54 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:6d320674513c355fec4e479ef93c5fd6bcd2bf0d3f66442201c70345297d0451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4765111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453df3ca98b0e352b1d2c17af5573a65251dc63b054697b0c10845c05fdf43e1`

```dockerfile
```

-	Layers:
	-	`sha256:5b9b732c4b7707ed9f951a8d70e83ad922878eb5e83ec627b4b11367ca5f348c`  
		Last Modified: Fri, 14 Nov 2025 04:36:34 GMT  
		Size: 4.7 MB (4730684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9574287e21a70046c79ee48a088e938769d84c379fcd6da38f656fc57ab1b8a`  
		Last Modified: Fri, 14 Nov 2025 04:36:35 GMT  
		Size: 34.4 KB (34427 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:2e3a03cd1b0bc2afd5113fad1b25af91107a5bba5a1b07a02ace47861f96fd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163042148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083f1f790bdb0d564d84ceb3e6e564081b2af494b8ccb79d3cbad012f4277f8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 12 Nov 2025 14:10:11 GMT
ENV container oci
# Wed, 12 Nov 2025 14:10:11 GMT
COPY dir:306690a4b33e0c2c47cf50b466ed471eb7ab206a490a8f74fd060934dfe49241 in /      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 14:10:12 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:0fb7b120ef84051a76f1b80ab468bcf42e6749f2d4faca4621e99b2ad0f6bb9a in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:0fb7b120ef84051a76f1b80ab468bcf42e6749f2d4faca4621e99b2ad0f6bb9a in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:10:12 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="09400c6ea1039bbeb186633c5815980c077ced2a" "org.opencontainers.image.revision"="09400c6ea1039bbeb186633c5815980c077ced2a" "build-date"="2025-11-12T14:09:54Z" "release"="1762956380"org.opencontainers.image.revision=09400c6ea1039bbeb186633c5815980c077ced2a
# Fri, 14 Nov 2025 01:30:00 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Fri, 14 Nov 2025 01:30:02 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:30:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 01:30:05 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 01:30:05 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Fri, 14 Nov 2025 01:30:05 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Fri, 14 Nov 2025 01:30:05 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.4 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Fri, 14 Nov 2025 01:30:05 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Nov 2025 01:30:05 GMT
ARG MARIADB_VERSION=11.8.4
# Fri, 14 Nov 2025 01:30:05 GMT
ENV MARIADB_VERSION=11.8.4
# Fri, 14 Nov 2025 01:30:29 GMT
# ARGS: MARIADB_VERSION=11.8.4
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Fri, 14 Nov 2025 01:30:29 GMT
VOLUME [/var/lib/mysql]
# Fri, 14 Nov 2025 01:30:29 GMT
# ARGS: MARIADB_VERSION=11.8.4
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 01:30:29 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 14 Nov 2025 01:30:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 01:30:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 01:30:29 GMT
USER mysql
# Fri, 14 Nov 2025 01:30:29 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 14 Nov 2025 01:30:29 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e01bb2a7f0e8ff512f86254e984d1cf0bdc9b357f1e0f0f61d352832dc12a646`  
		Last Modified: Wed, 12 Nov 2025 15:16:35 GMT  
		Size: 38.2 MB (38221043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3de148a370df58c84cbfd95ac6149fcf617923cb4fc0cb2ce66e0aa9580b20`  
		Last Modified: Fri, 14 Nov 2025 01:31:02 GMT  
		Size: 4.8 KB (4757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bea4f708528e5591cd2b0d8ad468984a56594c28f842900d3327aa61ee54fea`  
		Last Modified: Fri, 14 Nov 2025 01:31:03 GMT  
		Size: 2.0 MB (2004509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d609e34eaac14150a56212ab9242c39ec0be1fbaad5024c497985dda75ccf6a9`  
		Last Modified: Fri, 14 Nov 2025 01:31:03 GMT  
		Size: 6.0 MB (6046271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75049aee07188f08b39d7325ec5243dab1ca99658ead6f839fd5bb3280da907d`  
		Last Modified: Fri, 14 Nov 2025 01:31:03 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4870e9cb0f69894c85868224a80e5dfe59f75a6ba3d54c163bc4b6120fadd8cd`  
		Last Modified: Fri, 14 Nov 2025 01:31:03 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f17a0c99ce7f995c3c678b70deea00728413f73372c05219cef5c24a421b017`  
		Last Modified: Fri, 14 Nov 2025 01:31:21 GMT  
		Size: 116.8 MB (116752391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636001571a7df88233e453f3e9443987bf649b6af1306872670666f1f4da966f`  
		Last Modified: Fri, 14 Nov 2025 01:31:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e500008d84eb108fdde9651da7e281644663b315740d27b51c2c5065f1fd2c80`  
		Last Modified: Fri, 14 Nov 2025 01:31:02 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c56d8812cbad2f5e251b283ff2ccb68e991ffc0923979af5d80d723b21af4e`  
		Last Modified: Fri, 14 Nov 2025 01:31:02 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:11a0b5117929a6b4b210862a6a6446a027a6f3542bdd9d8b92b2c25237d416d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4764152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01378ccc0f8bb5323a2101c1f5ab944e69608541e085f3867f9cde3393bb70bd`

```dockerfile
```

-	Layers:
	-	`sha256:e88fce20852e5d4d9f8f8fcb8013888d1b13b8ab7392221214894f8fdf074703`  
		Last Modified: Fri, 14 Nov 2025 04:36:40 GMT  
		Size: 4.7 MB (4729519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf9b668311bda155dd3575284f754d6e14ac4af0f5be7f0e4de7888e9a0578b4`  
		Last Modified: Fri, 14 Nov 2025 04:36:41 GMT  
		Size: 34.6 KB (34633 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:73bfe9b6eeace7780ad62ce93a533e05bf3d62535d6e3f67997d624843e6ba39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178303735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44613a5d12f0289bf253f098e8b71ea2dea73b7d560f9f0dab7a5f330796f1a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 12 Nov 2025 14:16:19 GMT
ENV container oci
# Wed, 12 Nov 2025 14:16:20 GMT
COPY dir:b82b42d48fe8d3e110150627be797446b78337654b9b58113dd416e573c5a220 in /      
# Wed, 12 Nov 2025 14:16:20 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 14:16:20 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 14:16:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 14:16:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 14:16:20 GMT
COPY file:64a778769303615894b65a7e1f48ca07c19f426b240dc8585547e487e79b9119 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:16:20 GMT
COPY file:64a778769303615894b65a7e1f48ca07c19f426b240dc8585547e487e79b9119 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:16:21 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="09400c6ea1039bbeb186633c5815980c077ced2a" "org.opencontainers.image.revision"="09400c6ea1039bbeb186633c5815980c077ced2a" "build-date"="2025-11-12T14:16:09Z" "release"="1762956380"org.opencontainers.image.revision=09400c6ea1039bbeb186633c5815980c077ced2a
# Fri, 14 Nov 2025 03:23:34 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Fri, 14 Nov 2025 03:23:37 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Fri, 14 Nov 2025 03:23:42 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 03:23:42 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 03:23:43 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Fri, 14 Nov 2025 03:23:43 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Fri, 14 Nov 2025 03:23:43 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.4 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Fri, 14 Nov 2025 03:23:43 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Nov 2025 03:23:43 GMT
ARG MARIADB_VERSION=11.8.4
# Fri, 14 Nov 2025 03:23:43 GMT
ENV MARIADB_VERSION=11.8.4
# Fri, 14 Nov 2025 03:24:28 GMT
# ARGS: MARIADB_VERSION=11.8.4
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Fri, 14 Nov 2025 03:24:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 14 Nov 2025 03:24:28 GMT
# ARGS: MARIADB_VERSION=11.8.4
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 03:24:28 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 14 Nov 2025 03:24:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 03:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 03:24:28 GMT
USER mysql
# Fri, 14 Nov 2025 03:24:28 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 14 Nov 2025 03:24:28 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:179a593a6a9b7d7a22e6d6775d4ba55276bcd89646d198335c7dc5df13535e72`  
		Last Modified: Wed, 12 Nov 2025 18:10:57 GMT  
		Size: 44.5 MB (44458676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d54aa8ffd0df6715c0748e976789a1a5e80804fce03581cd8e39a6552799d33`  
		Last Modified: Fri, 14 Nov 2025 03:25:32 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976be9d9ec2d6e71bfb953cb784d1bfe1eecb2d4153ca87930158c831de239b4`  
		Last Modified: Fri, 14 Nov 2025 03:25:32 GMT  
		Size: 2.0 MB (2001433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18cff3b23dc94f27a3a839997f743bd41e3fe4dc5d8b79889cb8f7651e33dd2`  
		Last Modified: Fri, 14 Nov 2025 03:25:32 GMT  
		Size: 6.1 MB (6103774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bbb5f7a5c63bd8c3dae1df16bd658cbffa460966061659d64228c14e16f82d`  
		Last Modified: Fri, 14 Nov 2025 03:25:32 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b55ab5de59e4a6eab8b57209c84ceb41721a62993b347e90b958f138c5f283`  
		Last Modified: Fri, 14 Nov 2025 03:25:32 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95890834a1054840c57564ba917222814d3cefd0223379a278237a6044890cc`  
		Last Modified: Fri, 14 Nov 2025 03:25:48 GMT  
		Size: 125.7 MB (125721913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7809cae5c70524e2e7dcc42481fa2cbfc76340807c028cdc500578e683ff75`  
		Last Modified: Fri, 14 Nov 2025 03:25:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d30ad801db6a1b9f28b1b97ea3072fadc1b8da551715771c6ea9f5bdaeaf55`  
		Last Modified: Fri, 14 Nov 2025 03:25:32 GMT  
		Size: 4.0 KB (4034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f99b075470d0796e9cd35b2100668ca50f4742be6094d325c6ce92173795619`  
		Last Modified: Fri, 14 Nov 2025 03:25:32 GMT  
		Size: 8.4 KB (8393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:755a6d57d72f36c8eb80c9786bf0834229eb5b1a3090e31fd7be55376e67ccda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4759495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bd5c419925fba039e4c7418ac98c486d16f81cb184398b844cc80a5d743202`

```dockerfile
```

-	Layers:
	-	`sha256:94127d530f537b846a3f38f9616dc614f362155cae19633133c43602903222d4`  
		Last Modified: Fri, 14 Nov 2025 04:37:13 GMT  
		Size: 4.7 MB (4724998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88be3e264f1af8d63bc74125f87aab99bdb3cf927abb7f8f4b69ae080f0ab111`  
		Last Modified: Fri, 14 Nov 2025 04:37:14 GMT  
		Size: 34.5 KB (34497 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:1625a3d73fbbaf21212dcf04cd7f081f17854806319168d0cd957bc7817d7fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164955031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd77b19649302d100c7dd63e906040b342a72f94b7e6cc11b474b28efe3216d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 12 Nov 2025 14:23:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 14:23:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 14:23:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 14:23:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 14:23:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 14:23:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 14:23:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:23:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:23:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 12 Nov 2025 14:23:15 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 14:23:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 12 Nov 2025 14:23:15 GMT
ENV container oci
# Wed, 12 Nov 2025 14:23:15 GMT
COPY dir:8fb28e41f0652f38250d50e7c8b787f823f9c655088e3095ff5bb5e88ff8abdb in /      
# Wed, 12 Nov 2025 14:23:15 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 14:23:15 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 14:23:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 14:23:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 14:23:15 GMT
COPY file:871581d6a37c5961759af7dee95b7002ef35c09f77e017243a464bb731d06145 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:23:15 GMT
COPY file:871581d6a37c5961759af7dee95b7002ef35c09f77e017243a464bb731d06145 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:23:16 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="09400c6ea1039bbeb186633c5815980c077ced2a" "org.opencontainers.image.revision"="09400c6ea1039bbeb186633c5815980c077ced2a" "build-date"="2025-11-12T14:23:04Z" "release"="1762956380"org.opencontainers.image.revision=09400c6ea1039bbeb186633c5815980c077ced2a
# Fri, 14 Nov 2025 01:41:48 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Fri, 14 Nov 2025 01:41:50 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:41:54 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 01:41:54 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 01:41:55 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Fri, 14 Nov 2025 01:41:55 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Fri, 14 Nov 2025 01:41:55 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.4 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Fri, 14 Nov 2025 01:41:55 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Nov 2025 01:41:55 GMT
ARG MARIADB_VERSION=11.8.4
# Fri, 14 Nov 2025 01:41:55 GMT
ENV MARIADB_VERSION=11.8.4
# Fri, 14 Nov 2025 01:42:16 GMT
# ARGS: MARIADB_VERSION=11.8.4
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Fri, 14 Nov 2025 01:42:16 GMT
VOLUME [/var/lib/mysql]
# Fri, 14 Nov 2025 01:42:16 GMT
# ARGS: MARIADB_VERSION=11.8.4
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 01:42:16 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 14 Nov 2025 01:42:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 01:42:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 01:42:16 GMT
USER mysql
# Fri, 14 Nov 2025 01:42:16 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 14 Nov 2025 01:42:16 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d163f17b10d9f2c2fb3a866ba5330a41136f00b32975ee3b44f80939989d11e6`  
		Last Modified: Wed, 12 Nov 2025 18:10:56 GMT  
		Size: 38.1 MB (38137296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e59199033cad1b7e88361fee836681bf10437a9dd977d2f9b8b896642a1ccc`  
		Last Modified: Fri, 14 Nov 2025 01:43:00 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c1e75c8976ac6a4594ec248b06b1314cf620438e13c74e2d9143cb2a1af72b`  
		Last Modified: Fri, 14 Nov 2025 01:43:01 GMT  
		Size: 2.0 MB (2013621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96adbd2626996dd7afe84b92bcea78ff669464e8de9bba4aac91a5639e415b53`  
		Last Modified: Fri, 14 Nov 2025 01:43:01 GMT  
		Size: 6.1 MB (6136934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d0852e926854edd4d2aba26a19cb1eb43cbd16458c7b43d97e0b8670139c11`  
		Last Modified: Fri, 14 Nov 2025 01:43:01 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1258531bd70cdac5482818ff2d1e6fa6cb59fbc6396cab35b6646f6bdb43aa5`  
		Last Modified: Fri, 14 Nov 2025 01:43:01 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d9874b7b600d138a5a14895b1813cdce1c25001eb78984f0ffd98235c9a921`  
		Last Modified: Fri, 14 Nov 2025 01:43:18 GMT  
		Size: 118.6 MB (118649245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8ce8a9ed3c1f0de95a8958f2cf58bcf13916add28a97b39e75bdb07f17b3a3`  
		Last Modified: Fri, 14 Nov 2025 01:43:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747365450cc0ca772c8f5af9a0ce05b4190bd852290d90847f1cc16caf05898e`  
		Last Modified: Fri, 14 Nov 2025 01:43:01 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb379b4711d1ceb5f8242973bb836d0776c19a1833cb2cf58b97f2f1800e05b`  
		Last Modified: Fri, 14 Nov 2025 01:43:01 GMT  
		Size: 8.4 KB (8395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:0a01f4ebbc9bcdb099d4b9c791191712a18986a2097fcd45de6d323661d6776c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4753845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa467b76ba5953e6433ae1f49886ee728d8d77b44bcc2794b002bf45fbc00135`

```dockerfile
```

-	Layers:
	-	`sha256:3ca5d3843df848e2c8f3d42f6ed23c4cdf5ebbfcb8a8ef96fcf751873e36f2ae`  
		Last Modified: Fri, 14 Nov 2025 04:37:18 GMT  
		Size: 4.7 MB (4719418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edbba728cf74ebf428c34cac1fba789cfe44479c24d22ef9cfcedafe20147bea`  
		Last Modified: Fri, 14 Nov 2025 04:37:19 GMT  
		Size: 34.4 KB (34427 bytes)  
		MIME: application/vnd.in-toto+json
