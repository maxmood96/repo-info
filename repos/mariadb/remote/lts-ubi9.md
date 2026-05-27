## `mariadb:lts-ubi9`

```console
$ docker pull mariadb@sha256:a830ce68e188a55c189921a8093dac73bfa665021035baaa36c24fcbc1ca34bf
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

### `mariadb:lts-ubi9` - linux; amd64

```console
$ docker pull mariadb@sha256:565926f862137a501f5b27ed1e3076cda82e23addf2a17737b89992239b45f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163661978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a500a9b7060c57a0c531e77b7fccda035f9df8b77f197884fdd6dfee43fdae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 26 May 2026 15:32:20 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:32:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:32:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:32:21 GMT
ENV container oci
# Tue, 26 May 2026 15:32:22 GMT
COPY dir:bcf46f8211a223ea361ec9cb0b5d7567aaf9ce54beddfddade034948e142ca6d in /      
# Tue, 26 May 2026 15:32:22 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:32:22 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:32:22 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:32:02Z" "org.opencontainers.image.created"="2026-05-26T15:32:02Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:32:02Z
# Tue, 26 May 2026 23:11:24 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 26 May 2026 23:11:25 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 26 May 2026 23:11:28 GMT
ENV GOSU_VERSION=1.19
# Tue, 26 May 2026 23:11:28 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 May 2026 23:11:28 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 26 May 2026 23:11:28 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 26 May 2026 23:11:28 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.7 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 26 May 2026 23:11:28 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 26 May 2026 23:11:28 GMT
ARG MARIADB_VERSION=11.8.7
# Tue, 26 May 2026 23:11:28 GMT
ENV MARIADB_VERSION=11.8.7
# Tue, 26 May 2026 23:11:51 GMT
# ARGS: MARIADB_VERSION=11.8.7
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 26 May 2026 23:11:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 May 2026 23:11:51 GMT
# ARGS: MARIADB_VERSION=11.8.7
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 26 May 2026 23:11:51 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 26 May 2026 23:11:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 23:11:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 23:11:51 GMT
USER mysql
# Tue, 26 May 2026 23:11:51 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 26 May 2026 23:11:51 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:1a36cba5a1d845cee5e57e6f2dc9f828b4cc53403e207333e2220cd426126f13`  
		Last Modified: Tue, 26 May 2026 18:02:56 GMT  
		Size: 40.7 MB (40708696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bc65e3c365d54605f08d9c18c5e3bbb8a76f08739d6dec197c89de031b6bb7`  
		Last Modified: Tue, 26 May 2026 23:12:10 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63245deec3fece41c69e46ea9f4a4fd8c8603c02fc688742b7444bfd955da622`  
		Last Modified: Tue, 26 May 2026 23:12:11 GMT  
		Size: 2.0 MB (2006138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c6d6879c472da5fba3ef6b2c4b8ae537738d8748e46cd7caf3cdbbb6f9962c`  
		Last Modified: Tue, 26 May 2026 23:12:11 GMT  
		Size: 7.6 MB (7571152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073a4c8825c06040c92efb57726759ff51198a523c825c26670bfb84a121c67e`  
		Last Modified: Tue, 26 May 2026 23:12:11 GMT  
		Size: 299.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d12287113baf44fdc176922da11879aba224e7392726acf47531d144678a51`  
		Last Modified: Tue, 26 May 2026 23:12:12 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98c646c7d0e5fc7547061067d26e33040c3c264eeab2d26c0d7e425eed42bc`  
		Last Modified: Tue, 26 May 2026 23:12:15 GMT  
		Size: 113.4 MB (113358044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4539080fb272e6bc3b116d9fa574c6060d57371d4b1e495da64354815be5be1a`  
		Last Modified: Tue, 26 May 2026 23:12:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e95a25dffaea81e937219737a1ba85e3854956231701deb0b1480b333ba5828`  
		Last Modified: Tue, 26 May 2026 23:12:13 GMT  
		Size: 4.0 KB (4033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2ec4c821e17103968132771fc44626d7b5876b571edaa352ed38a4bf6d53cd`  
		Last Modified: Tue, 26 May 2026 23:12:13 GMT  
		Size: 8.4 KB (8409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:5a04e83f942d40d9a7bc4f6ef7fd641763fcf3406c1b23a4fc0ee9a4880cf3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4761358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf15ecb5667c3119f80d638b65c411e0d3769c3fc82488aafe5783782b10ced4`

```dockerfile
```

-	Layers:
	-	`sha256:3eb705edb3e05158dac39393c2c7d9e69a4329bd13fa0d75a47825b982d12553`  
		Last Modified: Tue, 26 May 2026 23:12:11 GMT  
		Size: 4.7 MB (4726910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a69c064a271060a62ac0d41cfb3ad28891f6548586c5374909f81a9396a3431a`  
		Last Modified: Tue, 26 May 2026 23:12:10 GMT  
		Size: 34.4 KB (34448 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi9` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a160698f10e8b9f1a894e6e95676fdd531db0d1e475343d6eceaac5d0dadf231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159314628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96fe05501c083a69bc1a18df9c478450a48840a8a0c1b9361adb7893284ecdd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 26 May 2026 15:34:04 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:34:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:34:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:34:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:34:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:34:05 GMT
ENV container oci
# Tue, 26 May 2026 15:34:06 GMT
COPY dir:9311212a31ee4f8d868b9de6ebae2a0a4e5d17aa2e21f16141915c8746951a19 in /      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:34:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:33:51Z" "org.opencontainers.image.created"="2026-05-26T15:33:51Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:33:51Z
# Tue, 26 May 2026 23:10:57 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 26 May 2026 23:10:58 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 26 May 2026 23:11:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 26 May 2026 23:11:01 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 May 2026 23:11:01 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 26 May 2026 23:11:01 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 26 May 2026 23:11:01 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.7 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 26 May 2026 23:11:01 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 26 May 2026 23:11:01 GMT
ARG MARIADB_VERSION=11.8.7
# Tue, 26 May 2026 23:11:01 GMT
ENV MARIADB_VERSION=11.8.7
# Tue, 26 May 2026 23:11:25 GMT
# ARGS: MARIADB_VERSION=11.8.7
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 26 May 2026 23:11:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 May 2026 23:11:25 GMT
# ARGS: MARIADB_VERSION=11.8.7
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 26 May 2026 23:11:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 26 May 2026 23:11:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 23:11:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 23:11:25 GMT
USER mysql
# Tue, 26 May 2026 23:11:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 26 May 2026 23:11:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:96e18ab71592420b36f7601002b695ecc23bf6b95f86193c23b2753544d31b8a`  
		Last Modified: Tue, 26 May 2026 18:00:10 GMT  
		Size: 38.8 MB (38840156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51036a80de39d3ce3e013d7929e3dd0e286d4b35e97579fb07711289dcbd6315`  
		Last Modified: Tue, 26 May 2026 23:11:45 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e225d46c312e76ce379a4ca8ac1f1b737c995e27fedaab69ccbb3340143e67`  
		Last Modified: Tue, 26 May 2026 23:11:45 GMT  
		Size: 2.0 MB (1997811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938064f7af15c04fd86ffa21b65d532e3b04fcb12b735271bbca19dd662d5ba3`  
		Last Modified: Tue, 26 May 2026 23:11:45 GMT  
		Size: 6.5 MB (6451164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d148e84c7b8da45cc7f2e5261b534b473159a709e03608626abad8bffcdc3a`  
		Last Modified: Tue, 26 May 2026 23:11:45 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc4d827c0ebe30c28cfe3805a4afd00cda842ac04f6c91b8a191e7a8c63de70`  
		Last Modified: Tue, 26 May 2026 23:11:47 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae5dbf85317ecdc6e2c10fa934aa062ccd5d43ebc589dd6ac8792cb8152d1d8`  
		Last Modified: Tue, 26 May 2026 23:11:49 GMT  
		Size: 112.0 MB (112007545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0eaaa777c6e4174bfccf51415fd6502042f230cc02067258ed6032c924b678c`  
		Last Modified: Tue, 26 May 2026 23:11:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f223326b8e6286df263ada363aec09929b4fa89d8c60b1e42c41520a1333cb`  
		Last Modified: Tue, 26 May 2026 23:11:47 GMT  
		Size: 4.0 KB (4033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971e924356c09c82e0ddf91c7fff872caeab7f81a8a7f4cc54093e2a9f12c118`  
		Last Modified: Tue, 26 May 2026 23:11:48 GMT  
		Size: 8.4 KB (8410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:e9723980558c889f31e9dc0fc0844d7e92522cb58099afa9e3c1f7b003b3c4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4760399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b43d5a1940f66d5e635e61d555e75c0267ffbfd03cabde2062485a2afc34d6`

```dockerfile
```

-	Layers:
	-	`sha256:8e1c09ed87269463c99fdddd5f3fda6450f6d087f6552a2a500d8972027af311`  
		Last Modified: Tue, 26 May 2026 23:11:45 GMT  
		Size: 4.7 MB (4725745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c962caa88f7caa2039dacec9ecc363852420213b6b458b6169631613c2f906c0`  
		Last Modified: Tue, 26 May 2026 23:11:45 GMT  
		Size: 34.7 KB (34654 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi9` - linux; ppc64le

```console
$ docker pull mariadb@sha256:44fdc1de76a1f16900dc93239154acc73451c99b7153feadd62c319bc367c9db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174254388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c71b09ce5c39a03e0fc1674d9ed3499c8001552168f3d4331cc5bde17adac9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 26 May 2026 15:33:29 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:33:29 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:33:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:33:29 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:33:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:33:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:33:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:33:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:33:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:33:29 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:33:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:33:29 GMT
ENV container oci
# Tue, 26 May 2026 15:33:30 GMT
COPY dir:5e813a184cbab7cbf1fee0022ee8e55aa80387ef4835bad3a6804243f83209e4 in /      
# Tue, 26 May 2026 15:33:30 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:33:30 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:33:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:33:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:33:30 GMT
COPY file:6f186cff34757f21b3d3a096028791fe755881607c0652e8eef706352323f06b in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:33:30 GMT
COPY file:6f186cff34757f21b3d3a096028791fe755881607c0652e8eef706352323f06b in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:33:30 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:33:18Z" "org.opencontainers.image.created"="2026-05-26T15:33:18Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:33:18Z
# Tue, 26 May 2026 23:20:28 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 26 May 2026 23:20:31 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 26 May 2026 23:20:36 GMT
ENV GOSU_VERSION=1.19
# Tue, 26 May 2026 23:20:36 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 May 2026 23:20:36 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 26 May 2026 23:20:36 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 26 May 2026 23:20:36 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.7 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 26 May 2026 23:20:36 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 26 May 2026 23:20:36 GMT
ARG MARIADB_VERSION=11.8.7
# Tue, 26 May 2026 23:20:36 GMT
ENV MARIADB_VERSION=11.8.7
# Tue, 26 May 2026 23:21:37 GMT
# ARGS: MARIADB_VERSION=11.8.7
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 26 May 2026 23:21:37 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 May 2026 23:21:38 GMT
# ARGS: MARIADB_VERSION=11.8.7
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 26 May 2026 23:21:39 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 26 May 2026 23:21:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 23:21:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 23:21:39 GMT
USER mysql
# Tue, 26 May 2026 23:21:39 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 26 May 2026 23:21:39 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f263dc8aecd57a446632c1e9df773e64bf709523e5ba6125cf199c6099e78689`  
		Last Modified: Tue, 26 May 2026 18:14:02 GMT  
		Size: 45.2 MB (45170860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bc234893eba9d178318a3dc09316a68393a069daaa1aca18eaea4b450460fc`  
		Last Modified: Tue, 26 May 2026 23:22:25 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20c5d0bcbde29c171a2be94a167b99b0dcfc4bce45d27ab045ad6623614f7cb`  
		Last Modified: Tue, 26 May 2026 23:22:26 GMT  
		Size: 2.0 MB (1999532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087791551fac1ad8a91287b0e150665541fd6ad97781a55d65cccafca813514c`  
		Last Modified: Tue, 26 May 2026 23:22:27 GMT  
		Size: 6.4 MB (6447780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cec273a42df86e79ca33745ddd747e9ba26bc1201338ad8105964fd5c17dc08`  
		Last Modified: Tue, 26 May 2026 23:22:25 GMT  
		Size: 302.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7155387ae679f3c306c47825f2af25751b977add925ab68096e4065d7f7d14`  
		Last Modified: Tue, 26 May 2026 23:22:27 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa23953187aa5e4552479cc77eec0c1f8a5d9cb70c3e46434ed8aabb397bfa43`  
		Last Modified: Tue, 26 May 2026 23:22:29 GMT  
		Size: 120.6 MB (120618270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28700d96d94543e9b368629abaf9f744c95627dd0f7b57f16b0c658a8f4e26cd`  
		Last Modified: Tue, 26 May 2026 23:22:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a080caa65fa10e76efc158c817fe877a18c131053c9d773e4fe6ca765da6f2`  
		Last Modified: Tue, 26 May 2026 23:22:28 GMT  
		Size: 4.0 KB (4030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e24ebfae2b6901d1fc887a9129c3d4a0093ed6ac42e3937819289ba782c10fa`  
		Last Modified: Tue, 26 May 2026 23:22:28 GMT  
		Size: 8.4 KB (8407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:237bf80892d4adee2f342c8466b030fe717d0fba5e14e9be627841c3a6fa25eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4755780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4058f9a25da2dd6542cb13e05ac4b03b39706e025061ea716c62af03befad3b0`

```dockerfile
```

-	Layers:
	-	`sha256:55bc237317ead8c688e3c453773297f2247c627d90424e1be18c4ecf31913aa4`  
		Last Modified: Tue, 26 May 2026 23:22:26 GMT  
		Size: 4.7 MB (4721262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16b43c91e7fd873a4feeada9277f8ef0c5b44b1d2e32746578831adf2371215`  
		Last Modified: Tue, 26 May 2026 23:22:25 GMT  
		Size: 34.5 KB (34518 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi9` - linux; s390x

```console
$ docker pull mariadb@sha256:b54ebe5735a273a643dc9829b44a92cb92bb2047c6ad5333649c0ed8a4104fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161132408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb008c403b1be69c63cd47abc3509dd1203ab8d7cbd1f1a03c8addb40d546f86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 26 May 2026 15:50:54 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:50:54 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:50:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:50:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:50:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:50:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:50:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:50:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:50:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:50:54 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:50:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:50:54 GMT
ENV container oci
# Tue, 26 May 2026 15:50:55 GMT
COPY dir:a00d53b24bbcf9097132390b191c936ff622d9b440a8f192754b910ebb84f566 in /      
# Tue, 26 May 2026 15:50:55 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:50:55 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:50:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:50:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:50:55 GMT
COPY file:48547272f4e6f96db66fd643aed1cfc9d3d7b7e696830a7dd166e3dd1a7a8aa4 in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:50:55 GMT
COPY file:48547272f4e6f96db66fd643aed1cfc9d3d7b7e696830a7dd166e3dd1a7a8aa4 in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:50:55 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:50:26Z" "org.opencontainers.image.created"="2026-05-26T15:50:26Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:50:26Z
# Tue, 26 May 2026 23:11:40 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 26 May 2026 23:11:43 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 26 May 2026 23:11:46 GMT
ENV GOSU_VERSION=1.19
# Tue, 26 May 2026 23:11:46 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 May 2026 23:11:46 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 26 May 2026 23:11:46 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 26 May 2026 23:11:46 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.7 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 26 May 2026 23:11:46 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 26 May 2026 23:11:46 GMT
ARG MARIADB_VERSION=11.8.7
# Tue, 26 May 2026 23:11:46 GMT
ENV MARIADB_VERSION=11.8.7
# Tue, 26 May 2026 23:12:12 GMT
# ARGS: MARIADB_VERSION=11.8.7
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 26 May 2026 23:12:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 May 2026 23:12:12 GMT
# ARGS: MARIADB_VERSION=11.8.7
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 26 May 2026 23:12:12 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 26 May 2026 23:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 23:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 23:12:12 GMT
USER mysql
# Tue, 26 May 2026 23:12:12 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 26 May 2026 23:12:12 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6ba40b0a7d8c65538d55968f5725eca287bda3024401d2f12b225797f497e32b`  
		Last Modified: Tue, 26 May 2026 18:13:55 GMT  
		Size: 38.8 MB (38794791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940fd698a37242083e076887898dd1ea08c57c3d34ec9288d63542d01ea1dcac`  
		Last Modified: Tue, 26 May 2026 23:12:47 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd04d459dbb4076e1d2f64479cab666690402e602b6d217a96bdd35dac57aad6`  
		Last Modified: Tue, 26 May 2026 23:12:47 GMT  
		Size: 2.0 MB (2018368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b897fe8f35051914aa960bb8decc6cff140633be32206d139f114ceada8901`  
		Last Modified: Tue, 26 May 2026 23:12:48 GMT  
		Size: 6.5 MB (6479252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606daee8ed8d89dd6305afe046e67f39a899b45e6981e686f5304081d2a8f6c7`  
		Last Modified: Tue, 26 May 2026 23:12:48 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8314f75ceee3eed5c0b68e32dba5a0db2c1be4566701b7ad26cdbc7c089b4f`  
		Last Modified: Tue, 26 May 2026 23:12:48 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43b0b63679c79403d09b8a8ae3a1a6ff91688c4ab2e508e5df4c698793674cf`  
		Last Modified: Tue, 26 May 2026 23:12:50 GMT  
		Size: 113.8 MB (113822045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80234a47b983f88b6362578b61c604cb6ceddc6637d087e28ad9a4d3d8fe03c6`  
		Last Modified: Tue, 26 May 2026 23:12:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e22f7547f2964238e805935f58e3a43d50a4104ecbe3ac55bf11be32008173`  
		Last Modified: Tue, 26 May 2026 23:12:49 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d1a8f62fcb3e74a91b3be29a7a663d9cf511131e1557701692641a36fd7d3b`  
		Last Modified: Tue, 26 May 2026 23:12:49 GMT  
		Size: 8.4 KB (8410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:72124c49d3e1ba16f08f321d1e6df1d87078568d393bc448846d27fce9da6e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4750092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2004952ec3184ce24be38cf112bdde23e77a89e540363c9e363167ee9e3f38`

```dockerfile
```

-	Layers:
	-	`sha256:21d20236cf03d621cd37d7a95dc08996afd86449cadac170016873efced42491`  
		Last Modified: Tue, 26 May 2026 23:12:47 GMT  
		Size: 4.7 MB (4715644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6aa5900b52c7508687d6d604ac93bee23a9354ec40bae85ead311143f5406e0`  
		Last Modified: Tue, 26 May 2026 23:12:47 GMT  
		Size: 34.4 KB (34448 bytes)  
		MIME: application/vnd.in-toto+json
