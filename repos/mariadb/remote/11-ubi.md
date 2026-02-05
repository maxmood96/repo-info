## `mariadb:11-ubi`

```console
$ docker pull mariadb@sha256:e5634db16ed3053333a7fd8b704c11b654faaacc3f8288f6578c82e5d670db4a
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
$ docker pull mariadb@sha256:27722e20025fd47246e65f2560d5fdfbbde27602325189c55be2b7a794ec96e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167636581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e69b24c5cd4a9cf74db51749413b1b15784dce204504e4fec79a5ed02716054`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:16:43 GMT
ENV container oci
# Wed, 04 Feb 2026 11:16:43 GMT
COPY dir:e45f16623580cdab20a9c9f5e40207717eeb9bb3de78238f58a6f3e3c0582b7c in /      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:16:44 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:16:28Z" "org.opencontainers.image.created"="2026-02-04T11:16:28Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:16:28Z
# Thu, 05 Feb 2026 00:09:34 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Thu, 05 Feb 2026 00:09:36 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:09:39 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 00:09:39 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 00:09:39 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 05 Feb 2026 00:09:39 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 05 Feb 2026 00:09:39 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 05 Feb 2026 00:09:39 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 05 Feb 2026 00:09:39 GMT
ARG MARIADB_VERSION=11.8.5
# Thu, 05 Feb 2026 00:09:39 GMT
ENV MARIADB_VERSION=11.8.5
# Thu, 05 Feb 2026 00:10:02 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 05 Feb 2026 00:10:02 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 00:10:02 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Feb 2026 00:10:02 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 05 Feb 2026 00:10:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 00:10:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 00:10:02 GMT
USER mysql
# Thu, 05 Feb 2026 00:10:02 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 05 Feb 2026 00:10:02 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b6f39ea02118ec2218902231f7c1bd7f8869072595a1fc81ad65ced100bfe327`  
		Last Modified: Wed, 04 Feb 2026 12:07:03 GMT  
		Size: 40.0 MB (40009059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1658deb78ede2fa248856627451a4995b54720ee4b106d2311c3021d1e92748`  
		Last Modified: Thu, 05 Feb 2026 00:10:22 GMT  
		Size: 4.8 KB (4758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca17e2dd249aa96495c0effddbb1da03219a662526627f8d0c113f734e33969e`  
		Last Modified: Thu, 05 Feb 2026 00:10:22 GMT  
		Size: 2.0 MB (2006768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffde5c8ca48f9711b3db0a1ba538d3f003f810f6512e9942a60b387ae2b51d7`  
		Last Modified: Thu, 05 Feb 2026 00:10:22 GMT  
		Size: 7.2 MB (7202522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead869c078e6e97b0fe2af097bf81e6b342437c854a8a8ea3513597bba0f3f89`  
		Last Modified: Thu, 05 Feb 2026 00:10:22 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fc927887822284ee6dc2d30cd6e42bf15334eb4a5ef299166cb14727676df5`  
		Last Modified: Thu, 05 Feb 2026 00:10:23 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cb558c7d29976161055d63a029522f6747a600a8ab48ef7686a281d1d6fa5f`  
		Last Modified: Thu, 05 Feb 2026 00:10:26 GMT  
		Size: 118.4 MB (118400290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f14647a2b8b1fd475137e18cf6663f2740fa89051fbc7ea5028045f80bea458`  
		Last Modified: Thu, 05 Feb 2026 00:10:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f8dcb418de72d8d4c2640a436dc606b54fc574e77425a0c7fa521cc6200fb0`  
		Last Modified: Thu, 05 Feb 2026 00:10:23 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dd5b8861009084c78d8064dea18dd388270033633e46cd253f8a29edf80516`  
		Last Modified: Thu, 05 Feb 2026 00:10:24 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:8a2c3bdfe287a02d0d87249aa76d32bef84e47abb946b06e32a549a9b90e6240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4765865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7123dff97d32e404588a31a99a2e434687ca348916325b6f2d1878edb740af50`

```dockerfile
```

-	Layers:
	-	`sha256:cce414cd2efa5b0ae3bd28978249f5a76d125883d0ba81c26b5b15c3c89aff4a`  
		Last Modified: Thu, 05 Feb 2026 00:10:22 GMT  
		Size: 4.7 MB (4731439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f1040a0e6c533e69e9c039308259c60f839c4eeac072d6bf4cf587f651d0d65`  
		Last Modified: Thu, 05 Feb 2026 00:10:22 GMT  
		Size: 34.4 KB (34426 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5fb17175b0e298eabc7ffe7144c839ee20e0a99389e3037c529225a21dc0ed49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162938200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcac0d270d03151c37205fc1218552e802b38128dd1a4d4f0d8c9a2f752505a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:19:42 GMT
ENV container oci
# Wed, 04 Feb 2026 11:19:43 GMT
COPY dir:0c6fd0301db67da56e5ab3d7939a023e089cbf858b44dcb22c5b0ce99938dd88 in /      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:19:43 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:44 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:19:27Z" "org.opencontainers.image.created"="2026-02-04T11:19:27Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:19:27Z
# Thu, 05 Feb 2026 00:08:58 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Thu, 05 Feb 2026 00:09:00 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:09:03 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 00:09:03 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 00:09:03 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 05 Feb 2026 00:09:03 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 05 Feb 2026 00:09:03 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 05 Feb 2026 00:09:03 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 05 Feb 2026 00:09:03 GMT
ARG MARIADB_VERSION=11.8.5
# Thu, 05 Feb 2026 00:09:03 GMT
ENV MARIADB_VERSION=11.8.5
# Thu, 05 Feb 2026 00:09:29 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 05 Feb 2026 00:09:29 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 00:09:30 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Feb 2026 00:09:30 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 05 Feb 2026 00:09:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 00:09:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 00:09:30 GMT
USER mysql
# Thu, 05 Feb 2026 00:09:30 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 05 Feb 2026 00:09:30 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:afeee6a1a7760e6f32c7c8492fc015c48e0a3314849bd8e7fd5fd947d0f45087`  
		Last Modified: Wed, 04 Feb 2026 12:09:12 GMT  
		Size: 38.2 MB (38195721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe08313f554a7b5c0439d86cfef89d9104a90aa633bc808d796d649818c7a25`  
		Last Modified: Thu, 05 Feb 2026 00:09:51 GMT  
		Size: 4.8 KB (4758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba19fbec9a46b8a68e0f325938a9cd664c65da832120027dbdc1e744a73fcb9`  
		Last Modified: Thu, 05 Feb 2026 00:09:51 GMT  
		Size: 2.0 MB (2000431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968e6c0d78bbb5b5057631c1ae6703100efeca5ced85bc2fd5ad06baf636d7b9`  
		Last Modified: Thu, 05 Feb 2026 00:09:51 GMT  
		Size: 6.1 MB (6145265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e220113cfe37dac92ccadb3b188bae75fb9c7c64e8cad51c05097c21d68b18`  
		Last Modified: Thu, 05 Feb 2026 00:09:51 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2dd8e4770b74c47657f639b23368977010e7abe6fb575bf87cac193305e285`  
		Last Modified: Thu, 05 Feb 2026 00:09:52 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84130b08d7b3f605973479a23f552c5eba361897204a5cb2458cbe08b31b66fb`  
		Last Modified: Thu, 05 Feb 2026 00:09:55 GMT  
		Size: 116.6 MB (116578845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405ebf849d4a42d0e0be4ef25dbd355ffac477354920c097b5a044e7f5d75387`  
		Last Modified: Thu, 05 Feb 2026 00:09:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c770393e528723572da3ef36652ad4f95e46cc2adde7965a09ef25b7b16b476`  
		Last Modified: Thu, 05 Feb 2026 00:09:52 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610d728708aaf987237941a5439830c4e894e70c518ec1ee1ac032ec75223634`  
		Last Modified: Thu, 05 Feb 2026 00:09:53 GMT  
		Size: 8.4 KB (8395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:059bb2bb4713add10f6beefde7e31c6e8ce0e6c5f9d8edc61b65e653be077776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4764907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9de8c8ebb411a8f0fd9f64961cacef46d2ff094f6fca2f62f443ee79e3f5019`

```dockerfile
```

-	Layers:
	-	`sha256:58c3ce9e025b01ee46ec3e55252e4a87f827bb834b8be71099065380822889e7`  
		Last Modified: Thu, 05 Feb 2026 00:09:51 GMT  
		Size: 4.7 MB (4730274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d006047ddcf245304243e5149330b29036b8382b689ca22502afd6cd625ca03f`  
		Last Modified: Thu, 05 Feb 2026 00:09:51 GMT  
		Size: 34.6 KB (34633 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:c97318a8147cd9240de66eb7974e1ae88cfa4e0dd8955b8bc2298043c42002c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177905433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97556b5a04a5f38b82557691651bb7d17b5f55e16ecb7761a658ed3724a89603`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:18:55 GMT
ENV container oci
# Wed, 04 Feb 2026 11:18:56 GMT
COPY dir:ac22932cb19e0040fdd682ddcf58eafa9048ed80bbb0d7207ce4b58b9e8c1ce2 in /      
# Wed, 04 Feb 2026 11:18:56 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:18:56 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:18:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:18:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:18:56 GMT
COPY file:fc9edd6729debe0b8fd283950946b54a98819aab2c1a7de7861de07a73ecdf6a in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:18:57 GMT
COPY file:fc9edd6729debe0b8fd283950946b54a98819aab2c1a7de7861de07a73ecdf6a in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:18:57 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:18:45Z" "org.opencontainers.image.created"="2026-02-04T11:18:45Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:18:45Z
# Thu, 05 Feb 2026 01:30:17 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Thu, 05 Feb 2026 01:30:21 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 01:30:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 01:30:26 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 01:30:26 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 05 Feb 2026 01:30:27 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 05 Feb 2026 01:30:27 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 05 Feb 2026 01:30:27 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 05 Feb 2026 01:30:27 GMT
ARG MARIADB_VERSION=11.8.5
# Thu, 05 Feb 2026 01:30:27 GMT
ENV MARIADB_VERSION=11.8.5
# Thu, 05 Feb 2026 01:31:41 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 05 Feb 2026 01:31:41 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 01:31:42 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Feb 2026 01:31:44 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 05 Feb 2026 01:31:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 01:31:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 01:31:45 GMT
USER mysql
# Thu, 05 Feb 2026 01:31:45 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 05 Feb 2026 01:31:45 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9453cd9cf4ac5c59d91e7e792edc9ae031294feb6835b6b8c1c7fe6c37f48881`  
		Last Modified: Wed, 04 Feb 2026 12:09:30 GMT  
		Size: 44.5 MB (44463451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fdfc2186db63b32861670fc405c63305768dcc1ad016cf5d689827441d6e3e`  
		Last Modified: Thu, 05 Feb 2026 01:32:40 GMT  
		Size: 4.8 KB (4758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466788a69a26f7f774b600fe25eaf09d0392ef78540c27ccd8f26abcedc230e7`  
		Last Modified: Thu, 05 Feb 2026 01:32:41 GMT  
		Size: 2.0 MB (1997879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbe9f1b3303eac2400e6f7332402a0a68d1bbfd3ecf1b2bb1cd5cd6915db181`  
		Last Modified: Thu, 05 Feb 2026 01:32:41 GMT  
		Size: 6.1 MB (6145036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018dd0789465e96844c0ba29263339dab860d5415ff8f31e964ecdfa367539a2`  
		Last Modified: Thu, 05 Feb 2026 01:32:40 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d60a78dfa93468b9446b552eac1b11ded4d12cf9321809227e0522336d648d1`  
		Last Modified: Thu, 05 Feb 2026 01:32:42 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a208dce351062fda5abc448dfa5e9bc0e5c14e20db78addd11928e36b69595fe`  
		Last Modified: Thu, 05 Feb 2026 01:32:45 GMT  
		Size: 125.3 MB (125281121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1eaddf324919a5835adf7b0c30f37511dac5a671896c332ccf164aa9df90ac4`  
		Last Modified: Thu, 05 Feb 2026 01:32:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d5324b9c7f6341d4e8c2b0679c3d38531002bc5f8d84c9e9eba85b436b7d09`  
		Last Modified: Thu, 05 Feb 2026 01:32:42 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a2b4407149a7260cd1fea27528aca8649c6974629c5fcad46e2d396d3c3d50`  
		Last Modified: Thu, 05 Feb 2026 01:32:43 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:e0c0795e8e993638427218bda71f91201ec1590fed626946efeeef2425fd8f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4760250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5237bed9fe819311751844b510293c8534d8e2e269a31cac19bc57b222e45ccd`

```dockerfile
```

-	Layers:
	-	`sha256:1c4defcda9936c27a1a0688b177f8ab3dbd5340a7d152f5683f469339e3cb7a2`  
		Last Modified: Thu, 05 Feb 2026 01:32:41 GMT  
		Size: 4.7 MB (4725753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea91cda697d138a2a1c6c1b26613864b2a6c8b6019cf941c6e45736af68b6273`  
		Last Modified: Thu, 05 Feb 2026 01:32:40 GMT  
		Size: 34.5 KB (34497 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:c43cb38fe779064ae84920a64adb384a52bc43158c1981b0bfd61e82a93d1668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.1 MB (165052537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b99dab68b4f8b2489c5fddf7eab6fa8ec17b595358ef76477e30c8ccb8ee5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:28:10 GMT
ENV container oci
# Wed, 04 Feb 2026 11:28:10 GMT
COPY dir:ed1f066185517b0a2e4ef9432478916be75ee58442b799a2d0b87cd51ad8226a in /      
# Wed, 04 Feb 2026 11:28:10 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:28:10 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:28:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:28:11 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:28:11 GMT
COPY file:696c21c97fda61d0f3f09e274ba392676dba268826f34e2eb4e63f66e68bb97f in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:28:11 GMT
COPY file:696c21c97fda61d0f3f09e274ba392676dba268826f34e2eb4e63f66e68bb97f in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:28:11 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:27:14Z" "org.opencontainers.image.created"="2026-02-04T11:27:14Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:27:14Z
# Thu, 05 Feb 2026 00:11:10 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Thu, 05 Feb 2026 00:11:12 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:11:15 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 00:11:15 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 00:11:15 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 05 Feb 2026 00:11:15 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 05 Feb 2026 00:11:15 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 05 Feb 2026 00:11:15 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 05 Feb 2026 00:11:15 GMT
ARG MARIADB_VERSION=11.8.5
# Thu, 05 Feb 2026 00:11:15 GMT
ENV MARIADB_VERSION=11.8.5
# Thu, 05 Feb 2026 00:11:38 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 05 Feb 2026 00:11:38 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 00:11:38 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Feb 2026 00:11:38 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 05 Feb 2026 00:11:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 00:11:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 00:11:38 GMT
USER mysql
# Thu, 05 Feb 2026 00:11:38 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 05 Feb 2026 00:11:38 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a3073672938ee024c2e2b6308a166357e08b9d63db19f1301982940b3e05b9c5`  
		Last Modified: Wed, 04 Feb 2026 12:09:20 GMT  
		Size: 38.1 MB (38133403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daade0480370d3e7d2a98d04b2494facd7d933eaef5b4fc978d3991b9ce6bcc`  
		Last Modified: Thu, 05 Feb 2026 00:12:08 GMT  
		Size: 4.8 KB (4758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0685c1984534314337d12b5d0f916852e4dd3c0e5e1b6bc7aeba3774a349ccd`  
		Last Modified: Thu, 05 Feb 2026 00:12:09 GMT  
		Size: 2.0 MB (2012003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e025ca48b6995cd84c52d45227c3069265c5fd18ccb08fc904c096525f2150`  
		Last Modified: Thu, 05 Feb 2026 00:12:09 GMT  
		Size: 6.2 MB (6165507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9306fb6d54f55933476cbaa97409c5e52ee540a7eced252da3e73c07bac68e`  
		Last Modified: Thu, 05 Feb 2026 00:12:09 GMT  
		Size: 300.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8539c1f5313769f0eab1006dcda7c49c8158bf970b9e1bcbc788d1ce14d5ed`  
		Last Modified: Thu, 05 Feb 2026 00:12:09 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907308ae98bf20843f32f24962883218a47e60bdd4afd7014a662993c72a6b71`  
		Last Modified: Thu, 05 Feb 2026 00:12:12 GMT  
		Size: 118.7 MB (118723683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02de14aa1f607c4e561ea0a48e74e60c9f045f80f46997da35454731341fe659`  
		Last Modified: Thu, 05 Feb 2026 00:12:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb11a5ff4fa1c1aacfff4b7856970b21de58eb08aaf6829ec01972b1abda962b`  
		Last Modified: Thu, 05 Feb 2026 00:12:10 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f9dc10e6dcedd52d62fbcc61bb412ac04dd2799df5971daa08a69f86f55fc9`  
		Last Modified: Thu, 05 Feb 2026 00:12:10 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:e7090f2920fd750225a8c4ac9f2b2445b60c350c157f921836df5fbbaa69b09a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4754600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e78de831f5199dce075990ed9981b3404b2a173092b2962925e28c7bc8ae58`

```dockerfile
```

-	Layers:
	-	`sha256:7bd24252e56ecfc058492ed4e0f58296a391bef1c999b1e31e6d9005ab576028`  
		Last Modified: Thu, 05 Feb 2026 00:12:09 GMT  
		Size: 4.7 MB (4720173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66221ee266799c86088dd60fb239a1cd8804bad796eb58494255b4247189d445`  
		Last Modified: Thu, 05 Feb 2026 00:12:09 GMT  
		Size: 34.4 KB (34427 bytes)  
		MIME: application/vnd.in-toto+json
