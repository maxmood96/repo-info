## `mariadb:12-ubi`

```console
$ docker pull mariadb@sha256:df92c72eb31c3c24a52803c21b7e6d3ddce8a55b433351de39517157fee7c949
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

### `mariadb:12-ubi` - linux; amd64

```console
$ docker pull mariadb@sha256:8ae6494888077093465957c23e64a618346979c4c99edf7be7761220bed4b60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164573672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969db4dce57235faeacd22700d45e67bdd1ea34c269cafaeddb648eceed22938`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 02 Jun 2026 15:15:58 GMT
ENV container oci
# Tue, 02 Jun 2026 15:15:58 GMT
COPY dir:e8b072881a1b1351c3b2d1bd84c8a6d6b28cb6b00007243c1b82e61134e4db04 in /      
# Tue, 02 Jun 2026 15:15:58 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 15:15:58 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 15:15:59 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 15:15:59 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 15:15:59 GMT
COPY file:5abe2f7df4c217a707574e953fc9f76f54f8de027108bd9480e64819343fa499 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:15:59 GMT
COPY file:5abe2f7df4c217a707574e953fc9f76f54f8de027108bd9480e64819343fa499 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:15:59 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "org.opencontainers.image.revision"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "build-date"="2026-06-02T15:15:44Z" "org.opencontainers.image.created"="2026-06-02T15:15:44Z" "release"="1780413072"org.opencontainers.image.revision=2c7c4b29450f25f9bc18401f2298edead75bcd9f,org.opencontainers.image.created=2026-06-02T15:15:44Z
# Tue, 02 Jun 2026 22:46:17 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 02 Jun 2026 22:46:18 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:46:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Jun 2026 22:46:21 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jun 2026 22:46:21 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 02 Jun 2026 22:46:21 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 02 Jun 2026 22:46:21 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=12.3.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 02 Jun 2026 22:46:21 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.3.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 02 Jun 2026 22:46:21 GMT
ARG MARIADB_VERSION=12.3.2
# Tue, 02 Jun 2026 22:46:21 GMT
ENV MARIADB_VERSION=12.3.2
# Tue, 02 Jun 2026 22:46:43 GMT
# ARGS: MARIADB_VERSION=12.3.2
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-10 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export 7D8D15CBFC4E62688591FB2633D98517E37ED158 > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-10.noarch.rpm --output /tmp/epel-release-latest-10.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-10.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-10.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-10.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf install -y tzdata ; 	microdnf install --enablerepo=epel --disablerepo=mariadb --releasever=10.1 -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-galera-${MARIADB_VERSION} ; 	microdnf install -y galera-4 rsync grep gawk iproute coreutils-single findutils tar lsof socat; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 02 Jun 2026 22:46:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jun 2026 22:46:43 GMT
# ARGS: MARIADB_VERSION=12.3.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jun 2026 22:46:43 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 02 Jun 2026 22:46:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 22:46:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 22:46:43 GMT
USER mysql
# Tue, 02 Jun 2026 22:46:43 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 02 Jun 2026 22:46:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0e4e3984c47d80f8f7813d099ea4505637390207a530acceb3e7426232f7555a`  
		Last Modified: Tue, 02 Jun 2026 16:41:21 GMT  
		Size: 34.8 MB (34839018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc1ef2b205e051505c99d3beb2e9ae2bb59237ca174ea5e9de84339dae0794`  
		Last Modified: Tue, 02 Jun 2026 22:47:03 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c0be64c27ddbf7478a526f8bd51bc5e0c50c699e083c3897b3861184180331`  
		Last Modified: Tue, 02 Jun 2026 22:47:03 GMT  
		Size: 2.2 MB (2219310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abaca7d15605eaa75a23f9f292179cc3333f2588e05b18e24505eb5b02e27f1c`  
		Last Modified: Tue, 02 Jun 2026 22:47:03 GMT  
		Size: 10.0 MB (10017489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7783b17679a1c330ac157d79b44e3bd324dcb32be40e47705691952fd450c1`  
		Last Modified: Tue, 02 Jun 2026 22:47:03 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3689fa8bec42976dc885c893eecc24560435a0e9758af8d3d162d8df70147fc4`  
		Last Modified: Tue, 02 Jun 2026 22:47:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a75346e5be9e24f7c4eb35aef1da886d42b189ffdcd3e4cefc321ca43553f9`  
		Last Modified: Tue, 02 Jun 2026 22:47:07 GMT  
		Size: 117.5 MB (117479822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeb17a8bee6c7c8a77cdb170a807e3e25c8e796335ec412e452affaba4e0df2`  
		Last Modified: Tue, 02 Jun 2026 22:47:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585383eaf4fc112f95eab3b38ae32bb6ead949bf6a869aaba423172ac9430f41`  
		Last Modified: Tue, 02 Jun 2026 22:47:05 GMT  
		Size: 4.0 KB (4034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cd2d323601a1c530f244960724e9f36aca31aba28f46890d8416ffbbcb30ee`  
		Last Modified: Tue, 02 Jun 2026 22:47:05 GMT  
		Size: 8.5 KB (8493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:12-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:02f3278064111d1e8009670ef7773e84fb45a6e7755e725cb40a9940d88438f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8f948527346628358bd20169a00fad5b7b9dc20b9d176c7c598f40a6d0d201`

```dockerfile
```

-	Layers:
	-	`sha256:02e86eb85786f5d825377c82cf15fb20e7c82e514aec617b2a0b9833340f4d30`  
		Last Modified: Tue, 02 Jun 2026 22:47:03 GMT  
		Size: 4.9 MB (4899686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad278e8a22d25617528f652a0769cefbdb2667170a4b723101752b16b0fd4b6f`  
		Last Modified: Tue, 02 Jun 2026 22:47:03 GMT  
		Size: 35.0 KB (34982 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:12-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c725f0cb670df636e7201eefd0c20570a9d7b00fa72aa265cf8deef8c832faf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160387827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69f1180b0a1c096898121910c17d4c68c6d05455f30c09e3a84dd4a7395f588`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 02 Jun 2026 15:18:30 GMT
ENV container oci
# Tue, 02 Jun 2026 15:18:31 GMT
COPY dir:a6b2b21a8909319c9461e822bff140e3ef1b61d198a2f277660b14bd1d6a271f in /      
# Tue, 02 Jun 2026 15:18:31 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 15:18:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 15:18:31 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 15:18:31 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 15:18:31 GMT
COPY file:cdd42785ebb0fd2c525ecf4a97b6b97bf781caa3b4c77f748f3d95a5a6d4bb88 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:18:31 GMT
COPY file:cdd42785ebb0fd2c525ecf4a97b6b97bf781caa3b4c77f748f3d95a5a6d4bb88 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:18:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "org.opencontainers.image.revision"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "build-date"="2026-06-02T15:18:13Z" "org.opencontainers.image.created"="2026-06-02T15:18:13Z" "release"="1780413072"org.opencontainers.image.revision=2c7c4b29450f25f9bc18401f2298edead75bcd9f,org.opencontainers.image.created=2026-06-02T15:18:13Z
# Tue, 02 Jun 2026 22:45:48 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 02 Jun 2026 22:45:50 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:45:53 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Jun 2026 22:45:53 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jun 2026 22:45:53 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 02 Jun 2026 22:45:53 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 02 Jun 2026 22:45:53 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=12.3.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 02 Jun 2026 22:45:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.3.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 02 Jun 2026 22:45:53 GMT
ARG MARIADB_VERSION=12.3.2
# Tue, 02 Jun 2026 22:45:53 GMT
ENV MARIADB_VERSION=12.3.2
# Tue, 02 Jun 2026 22:46:16 GMT
# ARGS: MARIADB_VERSION=12.3.2
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-10 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export 7D8D15CBFC4E62688591FB2633D98517E37ED158 > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-10.noarch.rpm --output /tmp/epel-release-latest-10.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-10.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-10.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-10.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf install -y tzdata ; 	microdnf install --enablerepo=epel --disablerepo=mariadb --releasever=10.1 -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-galera-${MARIADB_VERSION} ; 	microdnf install -y galera-4 rsync grep gawk iproute coreutils-single findutils tar lsof socat; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 02 Jun 2026 22:46:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jun 2026 22:46:16 GMT
# ARGS: MARIADB_VERSION=12.3.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jun 2026 22:46:16 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 02 Jun 2026 22:46:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 22:46:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 22:46:16 GMT
USER mysql
# Tue, 02 Jun 2026 22:46:16 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 02 Jun 2026 22:46:16 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7cd594d4c3afe0f66eb7cfc2a31b3e461f371776f986ab3d5084853335f5d2f7`  
		Last Modified: Tue, 02 Jun 2026 16:41:21 GMT  
		Size: 33.0 MB (33037428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb76bc68e1121c38bc5c0d981f6007d3cb2bf6b8eb3e8d75e55d4f01b531944`  
		Last Modified: Tue, 02 Jun 2026 22:46:38 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a903df10e96ea05088cf06c41441a8a137157c6a57350a842cd372c202470223`  
		Last Modified: Tue, 02 Jun 2026 22:46:38 GMT  
		Size: 2.2 MB (2217932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9d47ed42fe01ebbbe72ec35555b09a0f49236c3e49fc1a0ba00c7101a2eb41`  
		Last Modified: Tue, 02 Jun 2026 22:46:38 GMT  
		Size: 9.8 MB (9810581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcc6cb613bd4c921adc13c167be01058cde28825ac4fcf9d1b5569bcec4ad76`  
		Last Modified: Tue, 02 Jun 2026 22:46:38 GMT  
		Size: 299.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91196c60e066c99597d9c59d865b2d9ffc0f2d0b2663dc4783f6c065c5d723c3`  
		Last Modified: Tue, 02 Jun 2026 22:46:39 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abfd2fd2da14fbfd4f3bd9324484e3e9f51c923a45e44bc4303fec11edcc76c`  
		Last Modified: Tue, 02 Jun 2026 22:46:42 GMT  
		Size: 115.3 MB (115303858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63770798f8f23ae756b388f98481e29905ca1c2bdcd291846866abbfa091e6c6`  
		Last Modified: Tue, 02 Jun 2026 22:46:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7e8da4a7fc61b9a295779b881381ee82be7ae13009a23b2d89fe5ef2b2cb05`  
		Last Modified: Tue, 02 Jun 2026 22:46:40 GMT  
		Size: 4.0 KB (4031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1941a8bade5b670588acdbfc14a9a5c81f7fcfb9f5304403a91cb4e7979c186`  
		Last Modified: Tue, 02 Jun 2026 22:46:40 GMT  
		Size: 8.5 KB (8491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:12-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:03be25df9bbbb2b1bedae32d704df9a0f7c79502fb024c1d8ec4d2f052e552af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f4660c110a13772f748a6822edd769c190a6759647e30d8c0515dee91090de`

```dockerfile
```

-	Layers:
	-	`sha256:3a3df9997c24ac3a93c0a0e8a991e6020e1170945537528b20dcf129659825d7`  
		Last Modified: Tue, 02 Jun 2026 22:46:38 GMT  
		Size: 4.9 MB (4899791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3d7e28433b498c6fa611de6cb3c016f237b9c27bcd7ef38d19536c651953cbc`  
		Last Modified: Tue, 02 Jun 2026 22:46:38 GMT  
		Size: 35.2 KB (35181 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:12-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:95e6f8d2b605815c9662c2c7c5fefacc99d97272f82a7de7cc35c7784b4cff32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175822583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b56ef392d27fca0410c4ab5fb1f607837cb8f09e96c7e74078868b07b02870`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Jun 2026 15:17:18 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 02 Jun 2026 15:17:19 GMT
ENV container oci
# Tue, 02 Jun 2026 15:17:19 GMT
COPY dir:92bfd12864edc92997d2d256b8a65c081538f9c2759c99ccd4aa8bcb0106a753 in /      
# Tue, 02 Jun 2026 15:17:19 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 15:17:19 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 15:17:19 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 15:17:19 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 15:17:20 GMT
COPY file:f48578db79ab4a61ea5f93f3a6d877bb461214fcd6d5322e90176aee654cbaf2 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:17:20 GMT
COPY file:f48578db79ab4a61ea5f93f3a6d877bb461214fcd6d5322e90176aee654cbaf2 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:17:20 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "org.opencontainers.image.revision"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "build-date"="2026-06-02T15:17:07Z" "org.opencontainers.image.created"="2026-06-02T15:17:07Z" "release"="1780413072"org.opencontainers.image.revision=2c7c4b29450f25f9bc18401f2298edead75bcd9f,org.opencontainers.image.created=2026-06-02T15:17:07Z
# Tue, 02 Jun 2026 22:59:09 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 02 Jun 2026 22:59:16 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:59:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Jun 2026 22:59:30 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jun 2026 22:59:31 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 02 Jun 2026 22:59:32 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 02 Jun 2026 22:59:32 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=12.3.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 02 Jun 2026 22:59:32 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.3.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 02 Jun 2026 22:59:32 GMT
ARG MARIADB_VERSION=12.3.2
# Tue, 02 Jun 2026 22:59:32 GMT
ENV MARIADB_VERSION=12.3.2
# Tue, 02 Jun 2026 23:00:59 GMT
# ARGS: MARIADB_VERSION=12.3.2
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-10 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export 7D8D15CBFC4E62688591FB2633D98517E37ED158 > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-10.noarch.rpm --output /tmp/epel-release-latest-10.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-10.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-10.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-10.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf install -y tzdata ; 	microdnf install --enablerepo=epel --disablerepo=mariadb --releasever=10.1 -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-galera-${MARIADB_VERSION} ; 	microdnf install -y galera-4 rsync grep gawk iproute coreutils-single findutils tar lsof socat; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 02 Jun 2026 23:00:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jun 2026 23:01:00 GMT
# ARGS: MARIADB_VERSION=12.3.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jun 2026 23:01:02 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 02 Jun 2026 23:01:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 23:01:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 23:01:03 GMT
USER mysql
# Tue, 02 Jun 2026 23:01:03 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 02 Jun 2026 23:01:03 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f64094e3e3609aa276182d8f78ae91793a4e608c47e7c897b908d4be321f6cb0`  
		Last Modified: Tue, 02 Jun 2026 18:16:23 GMT  
		Size: 39.0 MB (38987518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2412fab308440e94d98de17ed584eff238146347d2b8882ee208185f4fd9800`  
		Last Modified: Tue, 02 Jun 2026 23:02:17 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96529078a734259888b741068fc5d136b695cf05311a474ef88b1bc74de5d062`  
		Last Modified: Tue, 02 Jun 2026 23:02:17 GMT  
		Size: 2.2 MB (2244764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105ade9c1908096d52406a29f2f798da88172ef4a17959b80d7a1d0eaa19c7b2`  
		Last Modified: Tue, 02 Jun 2026 23:02:17 GMT  
		Size: 10.5 MB (10489692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b45224c4b3fb74c51eb6435d412506640509a1e9e796ade7788ab189d7cddb`  
		Last Modified: Tue, 02 Jun 2026 23:02:17 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb9838c60e7ef7867cda6ff30b267a43af2bdfa615d80c4369836f6ad3878ca`  
		Last Modified: Tue, 02 Jun 2026 23:02:20 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eea0648aa663a85a673b7388ddfd04bcf3406952ae7ed65285678b02ed5ea6e`  
		Last Modified: Tue, 02 Jun 2026 23:02:24 GMT  
		Size: 124.1 MB (124082571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfab1e6566a344c8c79b8d5bc47e552bac6f098f7fa5ce076206b087b54bb4e2`  
		Last Modified: Tue, 02 Jun 2026 23:02:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cf40fa856588c6cb9c2d39627a3fcc7ffb5412fa3a901481e63a750012b311`  
		Last Modified: Tue, 02 Jun 2026 23:02:20 GMT  
		Size: 4.0 KB (4033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc464ac33f0e4e09a9375a7db66c4f6b834d64d064dffc29fbf0f08ebdc9c426`  
		Last Modified: Tue, 02 Jun 2026 23:02:20 GMT  
		Size: 8.5 KB (8493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:12-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:7016458b1a525c0ebe0ab4088206a582260c03223d85ec71b468e290bd8c437a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4923142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbee4be72c16daa307cd17679576f6a8fc59433e43788ef20e4efda118d50464`

```dockerfile
```

-	Layers:
	-	`sha256:5c5c0ea6214e7b99e80b549de51fa86d6e87a75365bdd2768a735ef3e5754dc6`  
		Last Modified: Tue, 02 Jun 2026 23:02:20 GMT  
		Size: 4.9 MB (4888889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:684aa614774209474543f9d98ec5b017be7e75509e50f4c7c2bb7da738bff08e`  
		Last Modified: Tue, 02 Jun 2026 23:02:20 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:12-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:726bcf7c95873fa09de63ed74778153203bd88069b0eaac705584a310964505d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.7 MB (170676851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c384ce1028a56fed1d9d4321118f89378f1d3a9fe3946962136c1bdf195d43d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 02 Jun 2026 15:29:16 GMT
ENV container oci
# Tue, 02 Jun 2026 15:29:16 GMT
COPY dir:0c85a1abf7afc52ab998b8b8163fb831aa7ce562a422231078f409e5a4c9ad75 in /      
# Tue, 02 Jun 2026 15:29:17 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 15:29:17 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 15:29:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 15:29:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 15:29:17 GMT
COPY file:e5fe3ee200e15ec67ab7a7520095c861775728fb94fefa880b9793f6fa30b055 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:29:17 GMT
COPY file:e5fe3ee200e15ec67ab7a7520095c861775728fb94fefa880b9793f6fa30b055 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:29:17 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "org.opencontainers.image.revision"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "build-date"="2026-06-02T15:28:33Z" "org.opencontainers.image.created"="2026-06-02T15:28:33Z" "release"="1780413072"org.opencontainers.image.revision=2c7c4b29450f25f9bc18401f2298edead75bcd9f,org.opencontainers.image.created=2026-06-02T15:28:33Z
# Tue, 02 Jun 2026 22:46:57 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Tue, 02 Jun 2026 22:46:59 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:47:03 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Jun 2026 22:47:03 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jun 2026 22:47:03 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Tue, 02 Jun 2026 22:47:03 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Tue, 02 Jun 2026 22:47:03 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=12.3.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Tue, 02 Jun 2026 22:47:03 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.3.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 02 Jun 2026 22:47:03 GMT
ARG MARIADB_VERSION=12.3.2
# Tue, 02 Jun 2026 22:47:03 GMT
ENV MARIADB_VERSION=12.3.2
# Tue, 02 Jun 2026 22:47:22 GMT
# ARGS: MARIADB_VERSION=12.3.2
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-10 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export 7D8D15CBFC4E62688591FB2633D98517E37ED158 > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-10.noarch.rpm --output /tmp/epel-release-latest-10.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-10.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-10.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-10.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf install -y tzdata ; 	microdnf install --enablerepo=epel --disablerepo=mariadb --releasever=10.1 -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-galera-${MARIADB_VERSION} ; 	microdnf install -y galera-4 rsync grep gawk iproute coreutils-single findutils tar lsof socat; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Tue, 02 Jun 2026 22:47:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jun 2026 22:47:23 GMT
# ARGS: MARIADB_VERSION=12.3.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jun 2026 22:47:23 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 02 Jun 2026 22:47:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 22:47:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 22:47:23 GMT
USER mysql
# Tue, 02 Jun 2026 22:47:23 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 02 Jun 2026 22:47:23 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:017341eabcfbc3839e70d99b30c5183e8f03952ba5046a4c9b68b4eff2e3021c`  
		Last Modified: Tue, 02 Jun 2026 18:16:12 GMT  
		Size: 34.7 MB (34725456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc8a906ed108cfe2a4b169e7e2046b89062fe55fe4fc5607a79b93de0b0f1b9`  
		Last Modified: Tue, 02 Jun 2026 22:47:58 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833d4cb615217f070beac1cc1cbe0a9d2724bac47ceba6cec3efbbce3557c474`  
		Last Modified: Tue, 02 Jun 2026 22:47:59 GMT  
		Size: 2.2 MB (2225055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4511a7b3e158472bc9641aeef83fc8c333b1ad393ad0fddafb690ae6fbf0d559`  
		Last Modified: Tue, 02 Jun 2026 22:47:59 GMT  
		Size: 10.2 MB (10155521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2325139b3aa2f656d9fa827cfb02c93cc5cebd87d045795a02a401345acbb8f`  
		Last Modified: Tue, 02 Jun 2026 22:47:58 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f94b11bf4b21ab76b895ba0f4ea98a6023ed2f7d72d8fcf3d3f2f63dc87ce5`  
		Last Modified: Tue, 02 Jun 2026 22:47:59 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bf2356b030c7a29bd5e80b7c30fa8bd1f7dabb1a75d3100f9326930467d672`  
		Last Modified: Tue, 02 Jun 2026 22:48:02 GMT  
		Size: 123.6 MB (123552792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2332e6aba70359f1107a4eddcbd7b41af59b55e8151ee0f21ba639a2e30167b`  
		Last Modified: Tue, 02 Jun 2026 22:48:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad797f770f59fa2f2ad0d2e6f910b056109bda4a7c343bc6fe5f37c266f41103`  
		Last Modified: Tue, 02 Jun 2026 22:48:00 GMT  
		Size: 4.0 KB (4031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d8774022703ed8b951dcfd0af0d5abbc330fbcc834f7ccb7f4b14e3a3f1a3c`  
		Last Modified: Tue, 02 Jun 2026 22:48:00 GMT  
		Size: 8.5 KB (8489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:12-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:9178fe0e03dabd5d44c9268a72abc31f3eade4af83325bf15e6c1d77e5411ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7081314e00dcfbac1a7de8822d839c34213385e6927e74de65f7d6dcdd20b12a`

```dockerfile
```

-	Layers:
	-	`sha256:72b03859f886861bfd9937d8517c2a66da28c8e9d6c789c7e1626b361bdb130f`  
		Last Modified: Tue, 02 Jun 2026 22:47:59 GMT  
		Size: 4.9 MB (4892798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe75de39439dd02217efee93cf2d5fe5fd86df00867929a99b20ad5e0dd33048`  
		Last Modified: Tue, 02 Jun 2026 22:47:58 GMT  
		Size: 35.0 KB (34982 bytes)  
		MIME: application/vnd.in-toto+json
