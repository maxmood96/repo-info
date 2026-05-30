## `mariadb:lts-ubi9`

```console
$ docker pull mariadb@sha256:29dd37f5df222f7c2668b51d412536ffeff0efc4d4b68d849e9bcead913bffe0
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
$ docker pull mariadb@sha256:13e8ef504f2da8748f378ecc3abbb3dcc9e4cbf8b29892334956c5854f13bdd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163670076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac2a5e27b580fcffc146a2d1487c8c53aff27c62d32d2ced8a83acf23317073`
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
# Fri, 29 May 2026 23:07:28 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Fri, 29 May 2026 23:07:30 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Fri, 29 May 2026 23:07:33 GMT
ENV GOSU_VERSION=1.19
# Fri, 29 May 2026 23:07:33 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 May 2026 23:07:33 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Fri, 29 May 2026 23:07:33 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Fri, 29 May 2026 23:07:33 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.8 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Fri, 29 May 2026 23:07:33 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.8 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 29 May 2026 23:07:33 GMT
ARG MARIADB_VERSION=11.8.8
# Fri, 29 May 2026 23:07:33 GMT
ENV MARIADB_VERSION=11.8.8
# Fri, 29 May 2026 23:07:55 GMT
# ARGS: MARIADB_VERSION=11.8.8
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Fri, 29 May 2026 23:07:55 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2026 23:07:55 GMT
# ARGS: MARIADB_VERSION=11.8.8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 29 May 2026 23:07:55 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 29 May 2026 23:07:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 29 May 2026 23:07:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2026 23:07:55 GMT
USER mysql
# Fri, 29 May 2026 23:07:55 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 29 May 2026 23:07:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:1a36cba5a1d845cee5e57e6f2dc9f828b4cc53403e207333e2220cd426126f13`  
		Last Modified: Tue, 26 May 2026 18:02:56 GMT  
		Size: 40.7 MB (40708696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35664cb695279f1d988fd6c3fc1222ede2a61f18d45e0c1f641ced81d246fb8`  
		Last Modified: Fri, 29 May 2026 23:08:15 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd29cd7e36dc6b3edb3228c21dabcb06796287107fb6d6d778b8460bb9e4e2b`  
		Last Modified: Fri, 29 May 2026 23:08:15 GMT  
		Size: 2.0 MB (2006145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be2caf5d7a261f4eb686faace3e3e4134b18cf2d463b5b8ba01da928234d68b`  
		Last Modified: Fri, 29 May 2026 23:08:15 GMT  
		Size: 7.6 MB (7566771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8b2f26d0a9b1c83b3273c91172fe49e385cbb4b36e23546fa878f1f0830174`  
		Last Modified: Fri, 29 May 2026 23:08:15 GMT  
		Size: 299.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccd8d0c8504afc8b2b8b7286d70cf3570e935d4754be77a4f51cefa26d460fe`  
		Last Modified: Fri, 29 May 2026 23:08:16 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1582c3d7882fc6a46674d34d8c0210aaa3b611daf1b47dc3525b94ddf7406b`  
		Last Modified: Fri, 29 May 2026 23:08:19 GMT  
		Size: 113.4 MB (113370427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff06073376d88cdcc80a8ba595081e170e5228a1b6d96e99f0fa76e19afbeba`  
		Last Modified: Fri, 29 May 2026 23:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff01a4f45324d373550b84db444a6d19d5362e676953eead51911a03c1f0dd9e`  
		Last Modified: Fri, 29 May 2026 23:08:17 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f267fe9b61ddbbea6c53766e7ae4f4a2f97b053ac18813e4613fe8a5b53a6238`  
		Last Modified: Fri, 29 May 2026 23:08:17 GMT  
		Size: 8.5 KB (8494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:15dbc8fe5d026128a4719f5b5762dbc0cc28f81bbe3cb151d707864e53ebee9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4761358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edc66b082f4230ec4704237b26e54a593f739c4996c9dc312b61a2d616e3c0e`

```dockerfile
```

-	Layers:
	-	`sha256:533cefc91e7bf3d787609917dc931c6d120592cea58b067312b62cbfdf0f2fc9`  
		Last Modified: Fri, 29 May 2026 23:08:15 GMT  
		Size: 4.7 MB (4726910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178209d37c1d02ba1df49616c82b2e0d325fe0c87aa39b9dd1474e4838ac0d27`  
		Last Modified: Fri, 29 May 2026 23:08:15 GMT  
		Size: 34.4 KB (34448 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi9` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:389819feb44f2e33fd30ba9046a0efe91c1c2836817a8f7e31f012d156dffc0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159318560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c830201c9bf9a7c678e32a65d229a61c2d0b58a0092f9dfab6490b28e130ad16`
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
# Fri, 29 May 2026 23:07:34 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Fri, 29 May 2026 23:07:36 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Fri, 29 May 2026 23:07:39 GMT
ENV GOSU_VERSION=1.19
# Fri, 29 May 2026 23:07:39 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 May 2026 23:07:39 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Fri, 29 May 2026 23:07:39 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Fri, 29 May 2026 23:07:39 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.8 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Fri, 29 May 2026 23:07:39 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.8 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 29 May 2026 23:07:39 GMT
ARG MARIADB_VERSION=11.8.8
# Fri, 29 May 2026 23:07:39 GMT
ENV MARIADB_VERSION=11.8.8
# Fri, 29 May 2026 23:08:02 GMT
# ARGS: MARIADB_VERSION=11.8.8
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Fri, 29 May 2026 23:08:02 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2026 23:08:02 GMT
# ARGS: MARIADB_VERSION=11.8.8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 29 May 2026 23:08:02 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 29 May 2026 23:08:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 29 May 2026 23:08:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2026 23:08:02 GMT
USER mysql
# Fri, 29 May 2026 23:08:02 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 29 May 2026 23:08:02 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:96e18ab71592420b36f7601002b695ecc23bf6b95f86193c23b2753544d31b8a`  
		Last Modified: Tue, 26 May 2026 18:00:10 GMT  
		Size: 38.8 MB (38840156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133cbe5b97b6c0e8117f8a09a306f2ef151dc088eed5ab4f7eba07f6d5bf591d`  
		Last Modified: Fri, 29 May 2026 23:08:22 GMT  
		Size: 4.8 KB (4761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff1268f8f165043edb69427ec5a55a25e1e1745eaa2cc47ced46396ff433b7c`  
		Last Modified: Fri, 29 May 2026 23:08:23 GMT  
		Size: 2.0 MB (1997790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f9aeb90bf7cde8dc5af79e159c14963f3da7ce05773aa220c1189052dd0630`  
		Last Modified: Fri, 29 May 2026 23:08:23 GMT  
		Size: 6.5 MB (6450931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5a7d2ef12b4b15180ffbc58d6bac501812a25c57364ef95df55d005ea082df`  
		Last Modified: Fri, 29 May 2026 23:08:23 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248191c23ff4a7d6940a3439c20868cca76b8d2d9e050eec230693f9efc736fe`  
		Last Modified: Fri, 29 May 2026 23:08:24 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26a7cee1c07c7413d9e4cd9482db70f76f6bdcf203d39af20d7926500424ebe`  
		Last Modified: Fri, 29 May 2026 23:08:26 GMT  
		Size: 112.0 MB (112011649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3e74108054f4a9a47ea8d848aa5ce0bde0bf49492a1951b1d869a1a4951614`  
		Last Modified: Fri, 29 May 2026 23:08:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b360c106da7dc326265794becac5f992eb450f3f5462c7087c6e99a26861474`  
		Last Modified: Fri, 29 May 2026 23:08:24 GMT  
		Size: 4.0 KB (4033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fc19505e5e34297804ad5ed3d23e0be3858a40b63b3211e98fa0aa62f0e208`  
		Last Modified: Fri, 29 May 2026 23:08:25 GMT  
		Size: 8.5 KB (8492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:08cf9f67d06d93005d6d81fb1b36b78a91e98c11fa5e253e0b1ae69e37ade666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4760398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80a44b3939ca9582a25a3d7d1b3c2ec83cba29ad5089e2b82c21fc9393f545d`

```dockerfile
```

-	Layers:
	-	`sha256:db63c6718836a5bc24063b0a48700480f0bcd6501937f1c3903cb7711b12e42c`  
		Last Modified: Fri, 29 May 2026 23:08:23 GMT  
		Size: 4.7 MB (4725745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:910d1f3423cdd6f3cd6fc600cd080f8d7939d187484720257c2285de8af214af`  
		Last Modified: Fri, 29 May 2026 23:08:23 GMT  
		Size: 34.7 KB (34653 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi9` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f25d29381124a17b97169305516430f6431c0ce9df94a87d99bf39253cce23ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174239645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98549763cc3cadd6faee933a9992d93797b942c17f31aa77f410689db588e1b1`
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
# Sat, 30 May 2026 02:10:03 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Sat, 30 May 2026 02:10:08 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Sat, 30 May 2026 02:10:14 GMT
ENV GOSU_VERSION=1.19
# Sat, 30 May 2026 02:10:14 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 30 May 2026 02:10:15 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Sat, 30 May 2026 02:10:15 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Sat, 30 May 2026 02:10:15 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.8 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Sat, 30 May 2026 02:10:15 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.8 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sat, 30 May 2026 02:10:15 GMT
ARG MARIADB_VERSION=11.8.8
# Sat, 30 May 2026 02:10:15 GMT
ENV MARIADB_VERSION=11.8.8
# Sat, 30 May 2026 02:11:00 GMT
# ARGS: MARIADB_VERSION=11.8.8
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Sat, 30 May 2026 02:11:00 GMT
VOLUME [/var/lib/mysql]
# Sat, 30 May 2026 02:11:01 GMT
# ARGS: MARIADB_VERSION=11.8.8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 30 May 2026 02:11:02 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sat, 30 May 2026 02:11:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 30 May 2026 02:11:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 30 May 2026 02:11:02 GMT
USER mysql
# Sat, 30 May 2026 02:11:02 GMT
EXPOSE map[3306/tcp:{}]
# Sat, 30 May 2026 02:11:02 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f263dc8aecd57a446632c1e9df773e64bf709523e5ba6125cf199c6099e78689`  
		Last Modified: Tue, 26 May 2026 18:14:02 GMT  
		Size: 45.2 MB (45170860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b4f9096b6271ae49cc8d27594f46c2b2fba4341ac8a93b0d7dd48cf11fbea`  
		Last Modified: Sat, 30 May 2026 02:11:44 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16396d58038fe32449882385b27f704ef23d1cfbf075364eeed6b8c49127186`  
		Last Modified: Sat, 30 May 2026 02:11:45 GMT  
		Size: 2.0 MB (1999524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108e98e6e1c339bde41746635d2401720ac3a7fd5526acdb52b06c2a6ef6467f`  
		Last Modified: Sat, 30 May 2026 02:11:45 GMT  
		Size: 6.4 MB (6446339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68812f76623abd47df716dec6eb62a6bd2f25fd372b29f7fb83c4d5006288b`  
		Last Modified: Sat, 30 May 2026 02:11:44 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4db9d6755315e7806a1ccdf6d22189cc801f906bcdf93dfcb3654dc220a77a`  
		Last Modified: Sat, 30 May 2026 02:11:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fca8f157836ffdeae51ca985412d19ea4b2db377c5698a45ccf73699ac8e09`  
		Last Modified: Sat, 30 May 2026 02:11:49 GMT  
		Size: 120.6 MB (120604888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6875e9197bdd35d972ac29f8c3aa5e12b4a3a740781fc89b732e6a8deaf7d628`  
		Last Modified: Sat, 30 May 2026 02:11:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fe381b2e91a61dd8c86c61fb210fba0fd5eb0b7fa37a337cdb6f7cb842ef77`  
		Last Modified: Sat, 30 May 2026 02:11:46 GMT  
		Size: 4.0 KB (4033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855ef8594f7568ed5e554ca7a8194a523fff651284827049c52974420a2f4931`  
		Last Modified: Sat, 30 May 2026 02:11:47 GMT  
		Size: 8.5 KB (8492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:c8b3af6b6b661ab8e45a6204b72b49b0790d553b67fbe8928fb2a1b37816440b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4755780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae3f8c8a42207e709d6fe3e0be9edfc5d192d96ec7a8d84658742fc16b68514`

```dockerfile
```

-	Layers:
	-	`sha256:b64cc6ef04226775d990c782324be72207165f39bdfb3ecd8f70fae01ed3ba42`  
		Last Modified: Sat, 30 May 2026 02:11:45 GMT  
		Size: 4.7 MB (4721262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e74e9d0aab7435fd8e26e0603be21b62ca7f29c7d09a6d3488e831f44936cf50`  
		Last Modified: Sat, 30 May 2026 02:11:44 GMT  
		Size: 34.5 KB (34518 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi9` - linux; s390x

```console
$ docker pull mariadb@sha256:e739a10b790e54fb86b97537249959693f9d0537b87f88b4d1fc2407e7035238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161134216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7024995fd33ece2499a666d54f4d5b665fa2b966a46de9da79953e07197fb5e`
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
# Fri, 29 May 2026 23:11:56 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Fri, 29 May 2026 23:11:58 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Fri, 29 May 2026 23:12:01 GMT
ENV GOSU_VERSION=1.19
# Fri, 29 May 2026 23:12:01 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 29 May 2026 23:12:01 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Fri, 29 May 2026 23:12:01 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Fri, 29 May 2026 23:12:01 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.8 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Fri, 29 May 2026 23:12:01 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.8 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 29 May 2026 23:12:01 GMT
ARG MARIADB_VERSION=11.8.8
# Fri, 29 May 2026 23:12:01 GMT
ENV MARIADB_VERSION=11.8.8
# Fri, 29 May 2026 23:12:33 GMT
# ARGS: MARIADB_VERSION=11.8.8
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Fri, 29 May 2026 23:12:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 29 May 2026 23:12:34 GMT
# ARGS: MARIADB_VERSION=11.8.8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 29 May 2026 23:12:34 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 29 May 2026 23:12:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 29 May 2026 23:12:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 May 2026 23:12:34 GMT
USER mysql
# Fri, 29 May 2026 23:12:34 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 29 May 2026 23:12:34 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:6ba40b0a7d8c65538d55968f5725eca287bda3024401d2f12b225797f497e32b`  
		Last Modified: Tue, 26 May 2026 18:13:55 GMT  
		Size: 38.8 MB (38794791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57070540e081be1270e65958f83f24aed7f49e1afed860b8cc6586a85bda218d`  
		Last Modified: Fri, 29 May 2026 23:13:10 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb213eada082a79b715bedc08bca56ee158c338e15accaf8899415384806ac3`  
		Last Modified: Fri, 29 May 2026 23:13:10 GMT  
		Size: 2.0 MB (2018368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f7815838b04721e204e1df5114cbed2ddb32260ce6a3f882227f7f661fe623`  
		Last Modified: Fri, 29 May 2026 23:13:10 GMT  
		Size: 6.5 MB (6477995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682e15f44eead08c52570c3c11c7424332521fb1c65d13fedf4b9ad37f01116d`  
		Last Modified: Fri, 29 May 2026 23:13:10 GMT  
		Size: 299.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c881787b0f444951363f922f019d2b6fb55c4af53e5dd67b7aeb7c203fc19ee`  
		Last Modified: Fri, 29 May 2026 23:13:11 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f390361b3853b729e9a20c4c3dae5797a436dc3386e348f414ed15cfa76ef7a`  
		Last Modified: Fri, 29 May 2026 23:13:14 GMT  
		Size: 113.8 MB (113825017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830a00296e5a6a99123f7b4fe304f1020f29d63f6431ae53ff93e0bb96d020a0`  
		Last Modified: Fri, 29 May 2026 23:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddb97e9c04e2c5a048cd8064130fbd1dc4fa7639cfc552ba2c929cebdbbeb5c`  
		Last Modified: Fri, 29 May 2026 23:13:11 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e137d2a0b9f5829ec82162de9f995fdc3c8050c16aa534d36aed02e97e13d2`  
		Last Modified: Fri, 29 May 2026 23:13:12 GMT  
		Size: 8.5 KB (8499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:6e6e97779a087c8c44863d0166b18c80a333df2aefff10eac721e90f6248555b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4750092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac0afa58c2518d792ebeb1fe06273299ee52a57fa17c76fbb5eab636f481c94`

```dockerfile
```

-	Layers:
	-	`sha256:2edcee74f3af562714eb63c5091f8cb97117c0cf51a429b32b2e96ec32165644`  
		Last Modified: Fri, 29 May 2026 23:13:10 GMT  
		Size: 4.7 MB (4715644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:544970823d7496ac8524177cab4b24ce42656e5ca56fef5a7246a6d91eb83203`  
		Last Modified: Fri, 29 May 2026 23:13:10 GMT  
		Size: 34.4 KB (34448 bytes)  
		MIME: application/vnd.in-toto+json
