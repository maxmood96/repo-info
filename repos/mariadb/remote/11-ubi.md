## `mariadb:11-ubi`

```console
$ docker pull mariadb@sha256:732e4b1e47b60bcbfa11e4bd10cf608a4fd560c0d91da81fe12bcb98b88e5d7b
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
$ docker pull mariadb@sha256:46d3ebb15f11fefc076648e3746457d47441ad01e8df18f445e4880e7de02f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.3 MB (167336258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6ca7e2f3055a369b2637efb7a42c1c8bb22ffc29722579dfbffd7b7ecdf480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 22 Jan 2026 05:12:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:50 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 05:12:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 05:12:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 05:13:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 05:13:01 GMT
ENV container oci
# Thu, 22 Jan 2026 05:13:09 GMT
COPY dir:de0fcf5c4847724050e2f935a6ca475ba4c6d0b18e49a32c8b2e370255fb563e in /      
# Thu, 22 Jan 2026 05:13:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 05:13:13 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 05:13:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 05:13:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 05:13:19 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:21 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:37 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T05:09:47Z" "org.opencontainers.image.created"="2026-01-22T05:09:47Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T05:09:47Z
# Mon, 26 Jan 2026 22:08:19 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Mon, 26 Jan 2026 22:08:20 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:08:24 GMT
ENV GOSU_VERSION=1.19
# Mon, 26 Jan 2026 22:08:24 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 26 Jan 2026 22:08:24 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Mon, 26 Jan 2026 22:08:24 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Mon, 26 Jan 2026 22:08:24 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Mon, 26 Jan 2026 22:08:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 26 Jan 2026 22:08:24 GMT
ARG MARIADB_VERSION=11.8.5
# Mon, 26 Jan 2026 22:08:24 GMT
ENV MARIADB_VERSION=11.8.5
# Mon, 26 Jan 2026 22:08:53 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Mon, 26 Jan 2026 22:08:53 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jan 2026 22:08:53 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 26 Jan 2026 22:08:53 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 26 Jan 2026 22:08:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:08:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:08:53 GMT
USER mysql
# Mon, 26 Jan 2026 22:08:53 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 26 Jan 2026 22:08:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216a4f1bb8de169eea2a4f9bd7380d3bee7ef923b455828ad62eea1be38b179f`  
		Last Modified: Mon, 26 Jan 2026 22:09:13 GMT  
		Size: 4.8 KB (4761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d690b28fb69034db2243fe094c7e30b858d3df59101f686929d62c8c1c7ed8d2`  
		Last Modified: Mon, 26 Jan 2026 22:09:13 GMT  
		Size: 2.0 MB (2006608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dbd46e0471553ef69651c33080e7c92b705b623f6f2c350c1f0a4fd3986f03`  
		Last Modified: Mon, 26 Jan 2026 22:09:13 GMT  
		Size: 7.2 MB (7196600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7ccdc6f18881af6d0cd60b9b5c718ac4cbc0ff2fe72ee37277ef030f88aa41`  
		Last Modified: Mon, 26 Jan 2026 22:09:13 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a08d29b4fdd91b20dc1df18bc062326300eb6ce573581d12f5547cc87bc805b`  
		Last Modified: Mon, 26 Jan 2026 22:09:14 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c520f39927e770d5f68c6e59ee0babc86d0d8b49a8edc4856a95b6c6364e0f1`  
		Last Modified: Mon, 26 Jan 2026 22:09:17 GMT  
		Size: 118.1 MB (118110091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e4dd3959c8acf6f28d8f29146db9f3b99a9ee64243b0847779c3578002982c`  
		Last Modified: Mon, 26 Jan 2026 22:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b887273794376191320823fe23e5f409a9060e0168e015b8d2edf0d8eac52a4c`  
		Last Modified: Mon, 26 Jan 2026 22:09:15 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0432fa7d34f59427f74ba3323ec9c60e5ea6b492ee87694a9cdcd56d108cb8`  
		Last Modified: Mon, 26 Jan 2026 22:09:15 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:92c84f323466df1d048d021d3c46a2b1c53b47abd406c36ba7b76a46ad2187b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4765030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef2e0ed642656ef393a70062c1975924d66069726b1e46e249238f0b39f7374`

```dockerfile
```

-	Layers:
	-	`sha256:2bde2325cb35d02b04d27e0674e2aa161c4427d0da76b8a65cfcd6bbdf12364b`  
		Last Modified: Mon, 26 Jan 2026 22:09:13 GMT  
		Size: 4.7 MB (4730603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:936ee71d9b1afbe82fa21442f988eabf2796af659144594ece2431050e62a23f`  
		Last Modified: Mon, 26 Jan 2026 22:09:13 GMT  
		Size: 34.4 KB (34427 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:487dc4c64fb9a2c68623942d45c22e229d331b8a2459dc7ec8871009a15d8080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162700124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627681924b566304f70f66fcd7c8bafb539b4a505e8db30aceec0f43f83c6274`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 04:47:00 GMT
ENV container oci
# Thu, 22 Jan 2026 04:47:00 GMT
COPY dir:5911db9f5450531429169fb3bc4d156204437f84bcda3e7b49af077219ecb148 in /      
# Thu, 22 Jan 2026 04:47:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 04:47:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T04:46:44Z" "org.opencontainers.image.created"="2026-01-22T04:46:44Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T04:46:44Z
# Mon, 26 Jan 2026 22:07:40 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Mon, 26 Jan 2026 22:07:41 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:07:45 GMT
ENV GOSU_VERSION=1.19
# Mon, 26 Jan 2026 22:07:45 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 26 Jan 2026 22:07:45 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Mon, 26 Jan 2026 22:07:45 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Mon, 26 Jan 2026 22:07:45 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Mon, 26 Jan 2026 22:07:45 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 26 Jan 2026 22:07:45 GMT
ARG MARIADB_VERSION=11.8.5
# Mon, 26 Jan 2026 22:07:45 GMT
ENV MARIADB_VERSION=11.8.5
# Mon, 26 Jan 2026 22:08:12 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Mon, 26 Jan 2026 22:08:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jan 2026 22:08:12 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 26 Jan 2026 22:08:12 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 26 Jan 2026 22:08:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:08:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:08:13 GMT
USER mysql
# Mon, 26 Jan 2026 22:08:13 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 26 Jan 2026 22:08:13 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7fa6f58d6e8018e6578e2a8b1e5f51c036adc282143dbc5a7b26cb19966155`  
		Last Modified: Mon, 26 Jan 2026 22:08:33 GMT  
		Size: 4.8 KB (4761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938737589b873996b29def4829aecaa7a3b8fae4d5f44175b0db6411ea61d948`  
		Last Modified: Mon, 26 Jan 2026 22:08:34 GMT  
		Size: 2.0 MB (1999936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d5ca21cfa6f6355388a646f0ba69ca119c381e003e5e51dc5a8df7b9cccb15`  
		Last Modified: Mon, 26 Jan 2026 22:08:34 GMT  
		Size: 6.1 MB (6142954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adca328c217bb0c6fc2897c17d824a674cb5fe044e250bf2af18d91ad5573d6`  
		Last Modified: Mon, 26 Jan 2026 22:08:33 GMT  
		Size: 300.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb10ca6e1db509927a65878db8f2accf524cb1f421d788bb0877d9ba31374591`  
		Last Modified: Mon, 26 Jan 2026 22:08:34 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e168dbbe351e55d102b400d2d59360810b72d9432ba88aacc3d9e9418f585e`  
		Last Modified: Mon, 26 Jan 2026 22:08:37 GMT  
		Size: 116.3 MB (116315661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0aad6e47af3321fc7f12d65651a474e24dcd4888c9f9479349457d41c58a0`  
		Last Modified: Mon, 26 Jan 2026 22:08:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e057be8f31f9059e1502844d2744ebacfbfeca9c52e4cadb716eefeaf75e40b8`  
		Last Modified: Mon, 26 Jan 2026 22:08:35 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faed2ae22e07a49449cc02e5354e409cd0f16961c38c5a22a498ad0832d1ec93`  
		Last Modified: Mon, 26 Jan 2026 22:08:36 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:4a2587c2029051f64053e4df8c00e76588ad2f15f3f3883e2d8b43b4623d43b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4764071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b52a6092da88367c87dcb6a89cbbfa6ae98f2cade440ced6ed9ca0d26fa1dc`

```dockerfile
```

-	Layers:
	-	`sha256:338c7674e3c467e888e14229a1f32d58f60dad5e2b259cf6f9ffcf504ff9cc5b`  
		Last Modified: Mon, 26 Jan 2026 22:08:34 GMT  
		Size: 4.7 MB (4729438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e852ce47de98ad437ec49c35e313b9a5af96ea803e64b32f0e80d51b8db02be`  
		Last Modified: Mon, 26 Jan 2026 22:08:33 GMT  
		Size: 34.6 KB (34633 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3b53bb5ca815d720d51c3ca5fc1ca0ac5adefad15b5639d49f7d9ff783807b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177554402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd64662cc694e41a17a83b9520f19a5df81a278d1dd13e0a4344fc6100ecb9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 01:08:41 GMT
ENV container oci
# Mon, 19 Jan 2026 01:08:42 GMT
COPY dir:3bd7ec6f425d769a16814adff3b957a15c4cbdec659c93cd45b1a546561564a3 in /      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 01:08:42 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:fe8dfccf0fa987a5d4946f1b72ab0cc09a6e656396d24bdd16b87ea3307e9302 in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:fe8dfccf0fa987a5d4946f1b72ab0cc09a6e656396d24bdd16b87ea3307e9302 in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 01:08:43 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T01:08:31Z" "org.opencontainers.image.created"="2026-01-19T01:08:31Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T01:08:31Z
# Tue, 20 Jan 2026 19:18:27 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 20 Jan 2026 19:18:31 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:18:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 20 Jan 2026 19:18:38 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 20 Jan 2026 19:18:39 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 20 Jan 2026 19:18:40 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 20 Jan 2026 19:18:40 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 20 Jan 2026 19:18:40 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 20 Jan 2026 19:18:40 GMT
ARG MARIADB_VERSION=11.8.5
# Tue, 20 Jan 2026 19:18:40 GMT
ENV MARIADB_VERSION=11.8.5
# Tue, 20 Jan 2026 19:19:53 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 20 Jan 2026 19:19:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 20 Jan 2026 19:19:55 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 20 Jan 2026 19:19:57 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 20 Jan 2026 19:19:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:19:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Jan 2026 19:19:59 GMT
USER mysql
# Tue, 20 Jan 2026 19:19:59 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 20 Jan 2026 19:19:59 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cb3df95d99fa30c8131b824671f0e15d0c34235a2e7bda21e4a361d100760346`  
		Last Modified: Mon, 19 Jan 2026 06:13:36 GMT  
		Size: 44.5 MB (44459713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17250368781b89b57b5ea27db64dbf8406b736b79eee40482d3ed7bc9fc0985`  
		Last Modified: Tue, 20 Jan 2026 19:21:05 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d836e627067aa0ec36f1f008a9a05c614b66e2019b41a3fbed185c274a23570`  
		Last Modified: Tue, 20 Jan 2026 19:21:05 GMT  
		Size: 2.0 MB (1999801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2696b452c5fed6c2cbf1df9164684017d3b524e0c4fd6f528b41cb847c2ba4`  
		Last Modified: Tue, 20 Jan 2026 19:21:06 GMT  
		Size: 6.1 MB (6143400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fda8d29429d7b8d2749bd91146ff4394fe40509541cd3356363a2cf06aa5496`  
		Last Modified: Tue, 20 Jan 2026 19:21:05 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a157bc97fa2ff9e4b17f436652817332b3bc4e28a2b64ec15375f2f0621625a`  
		Last Modified: Tue, 20 Jan 2026 19:21:06 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b96aeb3777c716b52054976ce94e19560e5b93b6adbcfc18f9d4d8d3834d0a`  
		Last Modified: Tue, 20 Jan 2026 19:21:10 GMT  
		Size: 124.9 MB (124933550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84192a629337f6f99e767ebcc2e5698ac189d9aa1232264c58b713397ebba41`  
		Last Modified: Tue, 20 Jan 2026 19:21:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f238a1e9f8b8b6bebfa1ba5919a63a3aaf0f7253525651098c349511e4cc1234`  
		Last Modified: Tue, 20 Jan 2026 19:21:07 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0a10ba7a611bc8a28e1ddba02663ce47728b5ec7fa9d6d2b83c37432d24f32`  
		Last Modified: Tue, 20 Jan 2026 19:21:08 GMT  
		Size: 8.4 KB (8395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:5769f53fd8583efd7d2d9f328f7976e587d09da4f24ded50565323437f4b463d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4759410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec5233bd361a0675e0cef25fd88d87c06e19e42d82b40d6d41ceb370f181d3a`

```dockerfile
```

-	Layers:
	-	`sha256:233ad3514f9bad0ba0de34919bc895114ff037790a096e8b327cc7afe60c8666`  
		Last Modified: Tue, 20 Jan 2026 19:21:05 GMT  
		Size: 4.7 MB (4724913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa95d311a92b86432b5bcf0c49d1f6e893717200aa5e07970a5f5704b2b07cd5`  
		Last Modified: Tue, 20 Jan 2026 19:21:05 GMT  
		Size: 34.5 KB (34497 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:79894043e6b8860e55dc44526f2cfffa02e228c8d3321b6a539f2f51ed9cb654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164747663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd7e6a8fb428ccc34f9578f17aa0269e2184a7fe68ef92c5aa004dd7019e41c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 19 Jan 2026 00:56:30 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:34 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:38 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:56:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:56:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:56:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:56:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:57:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:57:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:57:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:57:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:57:08 GMT
ENV container oci
# Mon, 19 Jan 2026 00:57:08 GMT
COPY dir:60e8b920663668133ad1c0beb8ddee0ed0404da0ad2cb12d0bdf023f3692297c in /      
# Mon, 19 Jan 2026 00:57:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:57:08 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:57:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:57:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:57:09 GMT
COPY file:3606e23b291d122a467fe42706adc9bb412f4262f39a03046011b69272713a85 in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:57:09 GMT
COPY file:3606e23b291d122a467fe42706adc9bb412f4262f39a03046011b69272713a85 in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:57:09 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:56:09Z" "org.opencontainers.image.created"="2026-01-19T00:56:09Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:56:09Z
# Tue, 20 Jan 2026 19:12:44 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 20 Jan 2026 19:12:46 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:12:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 20 Jan 2026 19:12:50 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 20 Jan 2026 19:12:50 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 20 Jan 2026 19:12:50 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 20 Jan 2026 19:12:50 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 20 Jan 2026 19:12:50 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 20 Jan 2026 19:12:50 GMT
ARG MARIADB_VERSION=11.8.5
# Tue, 20 Jan 2026 19:12:50 GMT
ENV MARIADB_VERSION=11.8.5
# Tue, 20 Jan 2026 19:13:16 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 20 Jan 2026 19:13:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 20 Jan 2026 19:13:16 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 20 Jan 2026 19:13:16 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 20 Jan 2026 19:13:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:13:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Jan 2026 19:13:16 GMT
USER mysql
# Tue, 20 Jan 2026 19:13:16 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 20 Jan 2026 19:13:16 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8d0fd9f50ed7506edfb499eb958eedd9d04f1fe7d6ebb11e4c454c579c856a27`  
		Last Modified: Mon, 19 Jan 2026 06:13:30 GMT  
		Size: 38.1 MB (38120160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de063497ffd42b0e7f4619471776ef4c6a806aa29761a2b199b31763b79444f8`  
		Last Modified: Tue, 20 Jan 2026 19:13:47 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e3a3611a95ec310336ab4e7c31eeba410672474c2d0566b676f26e3dacff31`  
		Last Modified: Tue, 20 Jan 2026 19:13:47 GMT  
		Size: 2.0 MB (2010196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2e2f56dba058ddff3aa654e9982e3c21729a786c7bb55e35fab951d7f88791`  
		Last Modified: Tue, 20 Jan 2026 19:13:47 GMT  
		Size: 6.2 MB (6166153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c668bb065083cf2a7a376617097cf3288a689dfab32026439791bd51838193`  
		Last Modified: Tue, 20 Jan 2026 19:13:47 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d83a218a829b32c418bf596073d1dd7d23c532bbd1d5dfbba7fb2a274732716`  
		Last Modified: Tue, 20 Jan 2026 19:13:48 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b54216e8e466324d75379c7a1790743825d30e07fe8dac90cd1318ea274a7f`  
		Last Modified: Tue, 20 Jan 2026 19:13:50 GMT  
		Size: 118.4 MB (118433212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16be72f14e2eb006c2bcc0ff5682b3668b74d33e29fe1494e920742cadbfab65`  
		Last Modified: Tue, 20 Jan 2026 19:13:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90854e671cd52fead45dd6709469315655b0d3f9cf7731611c953edfa309b900`  
		Last Modified: Tue, 20 Jan 2026 19:13:48 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d459ba5529bdecf0efd7b8e65283cc0722c7715ebcf833a2175f7beae46714`  
		Last Modified: Tue, 20 Jan 2026 19:13:49 GMT  
		Size: 8.4 KB (8395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:a687a3151956a71be2f8478a4fc58b41da465ca417cb6c7bd95ab435f258bc35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4753760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7534d4a27b839f6cc7d1faf6bebd5221077b31819b71a455282da3a3dc4243ca`

```dockerfile
```

-	Layers:
	-	`sha256:c99fe1d84760c652ba26e6019c91da5246dd83cf328ed4bc183dc4481b8c1155`  
		Last Modified: Tue, 20 Jan 2026 19:13:47 GMT  
		Size: 4.7 MB (4719333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:887a4b1fa1683f00ad39403318257133de8194b014d7690e8e5d72c765515740`  
		Last Modified: Tue, 20 Jan 2026 19:13:47 GMT  
		Size: 34.4 KB (34427 bytes)  
		MIME: application/vnd.in-toto+json
