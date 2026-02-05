## `mariadb:11-ubi`

```console
$ docker pull mariadb@sha256:99e97c3ac8d84e73297485e4bb0c8d409f35d32dd9fe070a252590cc894753aa
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
$ docker pull mariadb@sha256:a70e8f05ab4d0229c178046cb5407726d7cc1872683946460e98b39a62ca4556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167360640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9814b8062d1bfa8275b3024928e17d4152a20a5b53dfd3c4386283700d1b5395`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:57:26 GMT
ENV container oci
# Thu, 05 Feb 2026 04:57:27 GMT
COPY dir:045ee84cbf9f515d46f16866a480828e69331a2895b4a0d38aab70097694b23c in /      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:57:27 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:57:10Z" "org.opencontainers.image.created"="2026-02-05T04:57:10Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:57:10Z
# Thu, 05 Feb 2026 19:50:21 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Thu, 05 Feb 2026 19:50:22 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:50:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 19:50:25 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 19:50:25 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 05 Feb 2026 19:50:25 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 05 Feb 2026 19:50:25 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 05 Feb 2026 19:50:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 05 Feb 2026 19:50:25 GMT
ARG MARIADB_VERSION=11.8.5
# Thu, 05 Feb 2026 19:50:25 GMT
ENV MARIADB_VERSION=11.8.5
# Thu, 05 Feb 2026 19:50:50 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 19:50:50 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:50:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 19:50:50 GMT
USER mysql
# Thu, 05 Feb 2026 19:50:50 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 05 Feb 2026 19:50:50 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f5b60ea3b234d3169587f4127ec6855e8be2c29e3f0ef963207f1ea8be32f8d1`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 40.1 MB (40055891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e842eca7093ad2069d695567047c05f10df64f884de079af187ef7bdc8e73d`  
		Last Modified: Thu, 05 Feb 2026 19:51:11 GMT  
		Size: 4.8 KB (4757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8b7bbd20bb4b56bc21d47aafc9e02732e3e952161e5d1c5c1318af8e2dd25a`  
		Last Modified: Thu, 05 Feb 2026 19:51:11 GMT  
		Size: 2.0 MB (2000526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8692a98b2250e0f598d6a17396faf8c3d021137c53a0b39dfd727bdb72254bfb`  
		Last Modified: Thu, 05 Feb 2026 19:51:11 GMT  
		Size: 7.2 MB (7202349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d67ba235155d7c3658f6d8a1c53424c5143f3b4aefbcab55e26a4de71bcf27`  
		Last Modified: Thu, 05 Feb 2026 19:51:11 GMT  
		Size: 302.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7e325753d42ca54ab886c19b4bedc9112efea95c1fdd1b67a1fc160e5eb727`  
		Last Modified: Thu, 05 Feb 2026 19:51:12 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd4694b352675dde3b4bfe2708afdb41e69173cb9c0b806827676da9adbf72c`  
		Last Modified: Thu, 05 Feb 2026 19:51:20 GMT  
		Size: 118.1 MB (118083934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23658382f800bdb8f76069a826a12ff6f1f01c0e6c1b4e4d1502e6429da8638c`  
		Last Modified: Thu, 05 Feb 2026 19:51:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351e0f383b71bbfcb5ac14d540cc4cd7d0bac7395e2137220bfe10bb049a9eb3`  
		Last Modified: Thu, 05 Feb 2026 19:51:12 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeadc19f84ae37f1eb02eb656c1ed5b1220a48248f88c1a74b12622e0691c224`  
		Last Modified: Thu, 05 Feb 2026 19:51:13 GMT  
		Size: 8.4 KB (8395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:bf3cc2a7ca9587953f6bbb21d5ddc9c5e62fbc1a15ffdc9b2421d174c766bf33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4765082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d17a7d9f9b2f4a65713749f312f5e03ad42adfc4dfad9f1cb47e88520a2b00`

```dockerfile
```

-	Layers:
	-	`sha256:b6af7f603edc3456c40d0272515b2abf3c1cb18cb0d655b85f72d7ebe1c9027a`  
		Last Modified: Thu, 05 Feb 2026 19:51:11 GMT  
		Size: 4.7 MB (4730655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:350c9a50c9cf219b174fb089ab073e97436076f4d7699addbf92c0abaf47904e`  
		Last Modified: Thu, 05 Feb 2026 19:51:11 GMT  
		Size: 34.4 KB (34427 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8c44eecbd58fac3904813ad87a7376e56217147c60f1d73c96af21093a8268b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162625645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e7ce0ab995f92c51382f9981b1c5b24c3cb94b1d4467eb2c9dc1d828570558`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:59:52 GMT
ENV container oci
# Thu, 05 Feb 2026 04:59:53 GMT
COPY dir:7899936d8a255ef23a03d65107dd50f0ce4a76df58676bb1ea68c1d8f5eabde0 in /      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:59:53 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:59:37Z" "org.opencontainers.image.created"="2026-02-05T04:59:37Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:59:37Z
# Thu, 05 Feb 2026 19:50:08 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Thu, 05 Feb 2026 19:50:10 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:50:13 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 19:50:13 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 19:50:13 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 05 Feb 2026 19:50:13 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 05 Feb 2026 19:50:13 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 05 Feb 2026 19:50:13 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 05 Feb 2026 19:50:13 GMT
ARG MARIADB_VERSION=11.8.5
# Thu, 05 Feb 2026 19:50:13 GMT
ENV MARIADB_VERSION=11.8.5
# Thu, 05 Feb 2026 19:50:38 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 05 Feb 2026 19:50:38 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 19:50:38 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Feb 2026 19:50:38 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 05 Feb 2026 19:50:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:50:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 19:50:38 GMT
USER mysql
# Thu, 05 Feb 2026 19:50:38 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 05 Feb 2026 19:50:38 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:98b6d07e44e6381dc4b3ade3722986a976bbef5c5b424427e55892cfb27a03a0`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 38.2 MB (38215820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b210b1819fce3f967641cd10118af90d8f9a5e93ba615fb16a8cae4539344f9`  
		Last Modified: Thu, 05 Feb 2026 19:51:00 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af14bb373ee6c54de8eb48a3827f60d80b9344783dc1e3e40fb2c232d98ed2e`  
		Last Modified: Thu, 05 Feb 2026 19:51:00 GMT  
		Size: 2.0 MB (1994343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d661aa3761633224bc83e2b632b11eace35cf6be906f67d5dfd7c2de759497d`  
		Last Modified: Thu, 05 Feb 2026 19:51:00 GMT  
		Size: 6.1 MB (6143743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf9e6d75b94660ea14ddd19cf6fad7a964e40523100f61fbc10dd24fc7245f`  
		Last Modified: Thu, 05 Feb 2026 19:50:59 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec6a593461e79390e0ed2c0059be94898a6e3b87b2d092438ca2077e1b96d6f`  
		Last Modified: Thu, 05 Feb 2026 19:51:01 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8cf26ddba435937c78996608745f6eebb12722103163b1686d69123cb094be`  
		Last Modified: Thu, 05 Feb 2026 19:51:03 GMT  
		Size: 116.3 MB (116253803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efca49c300378b0a0b21ae898e53bf7db81d908759e632e481a6eb072b269eb`  
		Last Modified: Thu, 05 Feb 2026 19:51:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c16696196a8b6dbc2d2e504c3b4ca2ff457d5f02581d81cf75bb7d4574ccb1`  
		Last Modified: Thu, 05 Feb 2026 19:51:01 GMT  
		Size: 4.0 KB (4034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c00a09f0a2af29abb7395db117dd61c647729e91ab7376c633252e8bf1e4b11`  
		Last Modified: Thu, 05 Feb 2026 19:51:02 GMT  
		Size: 8.4 KB (8394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:ee3f2f28258b32d29739e7e7d61c055ef34af0f4ee8395094b7e1ad5f8d8b7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4764122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a354cc591f2ea6523d99c9b53b480652a9244e0b4271c85cbcb13bd4a59998f1`

```dockerfile
```

-	Layers:
	-	`sha256:4fcf577ff0b84ce190dcab59e40459bfb5dfb0d65709901bb4f9c6d8f68289c5`  
		Last Modified: Thu, 05 Feb 2026 19:51:00 GMT  
		Size: 4.7 MB (4729490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5503dab3458d3dadc932de09e794ebf98ffba5f9f53135305d85fbee8dad23ba`  
		Last Modified: Thu, 05 Feb 2026 19:51:00 GMT  
		Size: 34.6 KB (34632 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:6f81bf77aac045c9100f0150f9dd8af8b90b0f7590fd6712a4897a00339b7781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177505073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdfdfdada956a3ef67be7190df9ee4acd924ed41d01905ef16035f917ea0252`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 05:19:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 05:19:59 GMT
ENV container oci
# Thu, 05 Feb 2026 05:20:00 GMT
COPY dir:88b5851a77c5a8923c1135eccf97b07bb1b1d533881d05c9e3cd86d6a7a70b84 in /      
# Thu, 05 Feb 2026 05:20:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 05:20:00 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 05:20:00 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 05:20:00 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 05:20:00 GMT
COPY file:2deeab01ced2f311ec55a8229431b4137952c26bddd647f35c23005dfebf307c in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 05:20:00 GMT
COPY file:2deeab01ced2f311ec55a8229431b4137952c26bddd647f35c23005dfebf307c in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 05:20:01 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T05:19:48Z" "org.opencontainers.image.created"="2026-02-05T05:19:48Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T05:19:48Z
# Thu, 05 Feb 2026 19:52:05 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Thu, 05 Feb 2026 19:52:11 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:52:18 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 19:52:18 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 19:52:18 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 05 Feb 2026 19:52:18 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 05 Feb 2026 19:52:18 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 05 Feb 2026 19:52:18 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 05 Feb 2026 19:52:18 GMT
ARG MARIADB_VERSION=11.8.5
# Thu, 05 Feb 2026 19:52:18 GMT
ENV MARIADB_VERSION=11.8.5
# Thu, 05 Feb 2026 19:53:20 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 05 Feb 2026 19:53:20 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 19:53:23 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Feb 2026 19:53:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 05 Feb 2026 19:53:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:53:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 19:53:27 GMT
USER mysql
# Thu, 05 Feb 2026 19:53:27 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 05 Feb 2026 19:53:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4626d1a4e0f331b320f43bc1ebbec9d324207923aa2afcf48e14cccec11d1caf`  
		Last Modified: Thu, 05 Feb 2026 06:10:00 GMT  
		Size: 44.5 MB (44461525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872d2fcbd54698ba852a1b47bae1f447d1e6a61759c8ec71750129492188aaa2`  
		Last Modified: Thu, 05 Feb 2026 19:54:14 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771c971c3f7ff358cd05aabf96534ddafe4393d2ac060f8d708d59f4f5dea7f0`  
		Last Modified: Thu, 05 Feb 2026 19:54:15 GMT  
		Size: 2.0 MB (1994121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15384b7b3b8147bfad278e81220e98f59ae272885a4a824cffe23026b24dc30`  
		Last Modified: Thu, 05 Feb 2026 19:54:15 GMT  
		Size: 6.1 MB (6144988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842dace3bce3b02980f0454990b90fd946d615e20232d88add0e98f61c937877`  
		Last Modified: Thu, 05 Feb 2026 19:54:14 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866c0b3e37bb7176192efa93eae8405f6833eb8da481143aaf47d7e76619edc1`  
		Last Modified: Thu, 05 Feb 2026 19:54:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233f4119c8482d8ac220350d2e283cd832fb9a8ac9dcf886abc54092cd197911`  
		Last Modified: Thu, 05 Feb 2026 19:54:19 GMT  
		Size: 124.9 MB (124886496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0ab8ad09de07092d6671f8f146679f50e5aff7a387fbef24bb1a2205aea51d`  
		Last Modified: Thu, 05 Feb 2026 19:54:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25996229ed19b01c25f47082470f3f7592a9d32662f468d799ab77b2ac9a8af4`  
		Last Modified: Thu, 05 Feb 2026 19:54:16 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d4926018e4764ad6da04bc56cbbd582368a853267de19fd9c685e24c042f8b`  
		Last Modified: Thu, 05 Feb 2026 19:54:17 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:161523a0a0b60de5d45db10771d3a92671d15f879e732b143caea7abeb3fdb7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4759466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f4b8159377ca89139325d30aa469e4008e9bb364a7b0a2607ce014a1f9c131`

```dockerfile
```

-	Layers:
	-	`sha256:6e4aa0a6c75d128aea6e9813825623f079f54b277ff1ee3357b21cad3a83ffec`  
		Last Modified: Thu, 05 Feb 2026 19:54:15 GMT  
		Size: 4.7 MB (4724969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de1aded22af3980332c315aa3d9a9bc6e9716ab50eb84072532c6679a7f2469`  
		Last Modified: Thu, 05 Feb 2026 19:54:14 GMT  
		Size: 34.5 KB (34497 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:a5e744a760bdc3573b0c83884b95cef0009e48fb84b1e76eb6bbd9fa17b7e93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164729389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5879778a9a68f4a13e3592c8134d838c5f8779f660bce59ca221aca524b25986`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 05:17:51 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 05:17:51 GMT
ENV container oci
# Thu, 05 Feb 2026 05:17:52 GMT
COPY dir:0e0d0f454e08e5032aa10e9d7ae13a0cb2cd8a11785e0b58e1a01538558ce0cb in /      
# Thu, 05 Feb 2026 05:17:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 05:17:52 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 05:17:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 05:17:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 05:17:53 GMT
COPY file:748632c315c26c838fdb41aeb4c8e2a22097da0af431c7843ae16d688e0efb29 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 05:17:53 GMT
COPY file:748632c315c26c838fdb41aeb4c8e2a22097da0af431c7843ae16d688e0efb29 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 05:17:53 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T05:16:21Z" "org.opencontainers.image.created"="2026-02-05T05:16:21Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T05:16:21Z
# Thu, 05 Feb 2026 19:48:30 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Thu, 05 Feb 2026 19:48:31 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:48:35 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 19:48:35 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 19:48:35 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 05 Feb 2026 19:48:36 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 05 Feb 2026 19:48:36 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 05 Feb 2026 19:48:36 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 05 Feb 2026 19:48:36 GMT
ARG MARIADB_VERSION=11.8.5
# Thu, 05 Feb 2026 19:48:36 GMT
ENV MARIADB_VERSION=11.8.5
# Thu, 05 Feb 2026 19:49:03 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 05 Feb 2026 19:49:03 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 19:49:03 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Feb 2026 19:49:03 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 05 Feb 2026 19:49:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:49:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 19:49:03 GMT
USER mysql
# Thu, 05 Feb 2026 19:49:03 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 05 Feb 2026 19:49:03 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f61ab8e0b1fdec6911789bb1a925a7d3cc972464edb07d7ced8c2dff439f9138`  
		Last Modified: Thu, 05 Feb 2026 06:09:54 GMT  
		Size: 38.1 MB (38123371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2b8397a717244b13729bb0c248e6deadaa0047d079bcb542d8acd3c53e9b47`  
		Last Modified: Thu, 05 Feb 2026 19:49:36 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfceda04ec70f260e61ec26f8158a714fc53926369fec6e913c63a4cc7e75167`  
		Last Modified: Thu, 05 Feb 2026 19:49:37 GMT  
		Size: 2.0 MB (2010567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a040be7fbe5a338ec661421e44d2c8ee81ae8458b2379b54dd8364f2c1e09d`  
		Last Modified: Thu, 05 Feb 2026 19:49:37 GMT  
		Size: 6.2 MB (6167599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481fe53767595026921220c6d98f6553c4383884184f33a55bab42ee9bdc2e76`  
		Last Modified: Thu, 05 Feb 2026 19:49:42 GMT  
		Size: 299.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee0a2acbbf321f16b61a3d7b818471e2a381b2ac189eec77eb9454deadbace0`  
		Last Modified: Thu, 05 Feb 2026 19:49:37 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b77ddbf176ea590a7274241c2c446c0cb6077d15374bb89e7d322e162bcaf6d`  
		Last Modified: Thu, 05 Feb 2026 19:49:40 GMT  
		Size: 118.4 MB (118409912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef4ee0974070c8c13e5bb9ec4b866c15477267de7c835742d2a036d0bf374fd`  
		Last Modified: Thu, 05 Feb 2026 19:49:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb44b8c4a10248f366e7b854fd9fe290cffd2d5c97b429e135adc42a9bbf6b42`  
		Last Modified: Thu, 05 Feb 2026 19:49:38 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f790930015e0f184a994d919583cb7b4a4e77ff774ccaeecbcde1517dac38400`  
		Last Modified: Thu, 05 Feb 2026 19:49:39 GMT  
		Size: 8.4 KB (8395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:0ec7083e80c8727aabce431cfefb0cb944ba461b32bd65a6c908ddbf014f3dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4753816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f57a7cb9157f3cbb8a0052d1abcbf645368fed8053f5adbe9831ea52f05a5e8`

```dockerfile
```

-	Layers:
	-	`sha256:8578be2a52077df5f6da50adab77469d3ba57aa2c27a64599e03fd87adb55bca`  
		Last Modified: Thu, 05 Feb 2026 19:49:37 GMT  
		Size: 4.7 MB (4719389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:762c19cd0ce4427cd4ef80a9761a97d176ff79c7f8c6ab0c1c2ca998324d95b2`  
		Last Modified: Thu, 05 Feb 2026 19:49:36 GMT  
		Size: 34.4 KB (34427 bytes)  
		MIME: application/vnd.in-toto+json
