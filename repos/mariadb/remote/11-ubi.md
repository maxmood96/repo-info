## `mariadb:11-ubi`

```console
$ docker pull mariadb@sha256:e1606085f5ab00c21ee052dceb7318edb1eaaa3f58d0fc33cac0f54f784f1fb4
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
$ docker pull mariadb@sha256:07574779ff0129a2b63fdbb2ae7c06b93eb6f9334dbd6ef21b3105ecd34b1841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (167958625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5430bcd8d1920dbb9efea977101e7549ae21165eef7e7c68670e925c6ef2128`
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
# Mon, 17 Nov 2025 18:07:36 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Mon, 17 Nov 2025 18:07:37 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Mon, 17 Nov 2025 18:07:41 GMT
ENV GOSU_VERSION=1.19
# Mon, 17 Nov 2025 18:07:41 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 17 Nov 2025 18:07:41 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Mon, 17 Nov 2025 18:07:41 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Mon, 17 Nov 2025 18:07:41 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Mon, 17 Nov 2025 18:07:41 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 17 Nov 2025 18:07:41 GMT
ARG MARIADB_VERSION=11.8.5
# Mon, 17 Nov 2025 18:07:41 GMT
ENV MARIADB_VERSION=11.8.5
# Mon, 17 Nov 2025 18:08:10 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Mon, 17 Nov 2025 18:08:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 17 Nov 2025 18:08:11 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 17 Nov 2025 18:08:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 17 Nov 2025 18:08:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Nov 2025 18:08:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Nov 2025 18:08:11 GMT
USER mysql
# Mon, 17 Nov 2025 18:08:11 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 17 Nov 2025 18:08:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:179ba4be1de0701de7b39988f2989858194723f60b56b12f8d9438358e471a73`  
		Last Modified: Wed, 12 Nov 2025 15:07:23 GMT  
		Size: 40.0 MB (40048414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5d1884d899386637eb6aa76b35f3a961687d54b884d4c3fe5a8090099ce2a7`  
		Last Modified: Mon, 17 Nov 2025 18:09:06 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7816cfd7676185d5f5dd3cb8517e9ceaf79aa90a1f2552c4c1dfaed010a52d15`  
		Last Modified: Mon, 17 Nov 2025 18:09:07 GMT  
		Size: 2.0 MB (2010849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97d23496bf6e228180c81eed6fc58b1d1638bfc882fa4213c451363a35a719`  
		Last Modified: Mon, 17 Nov 2025 18:09:07 GMT  
		Size: 7.2 MB (7159071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fb68cd999b8a67c9140a2af446a123829331b35980225203fab6145b3e95be`  
		Last Modified: Mon, 17 Nov 2025 18:09:07 GMT  
		Size: 300.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73633a29f944bc45ea9c6f44a9d8ced504a135c6543b2ee68f442143697030b`  
		Last Modified: Mon, 17 Nov 2025 18:09:07 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc3119422cde1e8bfd2cd93743241f83d7edf02e60373e4e837ba04df9d7a97`  
		Last Modified: Mon, 17 Nov 2025 18:09:28 GMT  
		Size: 118.7 MB (118722355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d5d663b2982ccd3bfcb400ac64ab4474ac38077f4bcb0f7235bf277a3459bd`  
		Last Modified: Mon, 17 Nov 2025 18:09:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1e62ea55ada988dc1b4924d98f07bcbf83f62aaf56395a49890b21854455a2`  
		Last Modified: Mon, 17 Nov 2025 18:09:08 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a602177d5806df7ebba554179db9a603a9b771430be0241938c85fe840f709`  
		Last Modified: Mon, 17 Nov 2025 18:09:08 GMT  
		Size: 8.4 KB (8394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:08e80d496365b330e1b5937a796021ca27a25691510d9ba1ec97f2ef40155b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4765111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4470188b365e5d696b818996ff505337d4f64f6547df873a8d6450ec7e46cbf1`

```dockerfile
```

-	Layers:
	-	`sha256:b1a89eaaf91873b11f7ae6922ef627b5b887c925f21c9e464fe2baedc705fa94`  
		Last Modified: Mon, 17 Nov 2025 19:36:01 GMT  
		Size: 4.7 MB (4730684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5adb60fb7ca611576d2f2fcaa3f325ddabe96dbd1ecce66391a7261b21c3328`  
		Last Modified: Mon, 17 Nov 2025 19:36:02 GMT  
		Size: 34.4 KB (34427 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d0661e6cf55654eb1f9c67c5d012022c54a13a7cdd66aa8ae476102fd043e8d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163095597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab42be6eb7ef0e2f3367181a4695efbfe8944806754f408631b9df4c63f0b65`
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
# Mon, 17 Nov 2025 18:07:17 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Mon, 17 Nov 2025 18:07:18 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Mon, 17 Nov 2025 18:07:21 GMT
ENV GOSU_VERSION=1.19
# Mon, 17 Nov 2025 18:07:21 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 17 Nov 2025 18:07:21 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Mon, 17 Nov 2025 18:07:21 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Mon, 17 Nov 2025 18:07:21 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Mon, 17 Nov 2025 18:07:21 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 17 Nov 2025 18:07:21 GMT
ARG MARIADB_VERSION=11.8.5
# Mon, 17 Nov 2025 18:07:21 GMT
ENV MARIADB_VERSION=11.8.5
# Mon, 17 Nov 2025 18:07:45 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Mon, 17 Nov 2025 18:07:45 GMT
VOLUME [/var/lib/mysql]
# Mon, 17 Nov 2025 18:07:45 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 17 Nov 2025 18:07:45 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 17 Nov 2025 18:07:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Nov 2025 18:07:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Nov 2025 18:07:45 GMT
USER mysql
# Mon, 17 Nov 2025 18:07:45 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 17 Nov 2025 18:07:45 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e01bb2a7f0e8ff512f86254e984d1cf0bdc9b357f1e0f0f61d352832dc12a646`  
		Last Modified: Wed, 12 Nov 2025 15:16:35 GMT  
		Size: 38.2 MB (38221043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f002ff555688654d4070ad0741aba43b0f9d4efdb1a497a1d5434b05906a8f6`  
		Last Modified: Mon, 17 Nov 2025 18:08:32 GMT  
		Size: 4.8 KB (4761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac3def6a57b2febd34dd5c32cd905c850a4c6f48ee1461140e8bdc80b7c477f`  
		Last Modified: Mon, 17 Nov 2025 18:08:32 GMT  
		Size: 2.0 MB (2004507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686fe2780a7684dc594f6a5f311ac4010a5dbcabb4947e5e20bb262abaebd2fd`  
		Last Modified: Mon, 17 Nov 2025 18:08:33 GMT  
		Size: 6.1 MB (6108188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dca182330d2831ce4721fd8e32a066639eb721f362dee3bda7a5f2eef2e421`  
		Last Modified: Mon, 17 Nov 2025 18:08:32 GMT  
		Size: 300.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c88147abaf8e7a2e713f48e0a9de1fbe1b096835d3f157991a292ed59ca81c`  
		Last Modified: Mon, 17 Nov 2025 18:08:32 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4712a77d5b4aff2b244c956e3769eb52a3847181a06bb78e319652559d4dbe`  
		Last Modified: Mon, 17 Nov 2025 18:08:51 GMT  
		Size: 116.7 MB (116743921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc59d542581d4581e517932bf05590cc2403710a3ee56635ded049a772e06ccf`  
		Last Modified: Mon, 17 Nov 2025 18:08:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376a53dab88658450fe394d99e37149a9f0a5a082dae7c7f922d0f9aba7e2619`  
		Last Modified: Mon, 17 Nov 2025 18:08:32 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741d9f9adbea62391eda088e8856a689f00d03ebd7af0a753c85e075764101f5`  
		Last Modified: Mon, 17 Nov 2025 18:08:32 GMT  
		Size: 8.4 KB (8395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:dce308cd27b1bc5f6256a270db3503cf9251162e667915e837c4768074319781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4764152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70cf0cd73bcdcfd83b07276ae516b780c6d17cc9a4ffe5d16ebba26717e34a77`

```dockerfile
```

-	Layers:
	-	`sha256:261d865e9964c870f680e30d8d93fabb64add69ee1ca68e136f61592f36a9d87`  
		Last Modified: Mon, 17 Nov 2025 19:36:07 GMT  
		Size: 4.7 MB (4729519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f717de04664ede768ee9159bdcc074a3c721dbf34138f818798bb49a8a699c6`  
		Last Modified: Mon, 17 Nov 2025 19:36:09 GMT  
		Size: 34.6 KB (34633 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:c6468be7adb3eb5ba4bbe600b909f8e9ded7d04df896e0508a5bfadc12a5c3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178303825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14cb1080d92cdced2656cbcc4203089b8b39f63be7589d9d5022ef17c6bb39f7`
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
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Fri, 14 Nov 2025 03:23:43 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Nov 2025 03:23:43 GMT
ARG MARIADB_VERSION=11.8.5
# Fri, 14 Nov 2025 03:23:43 GMT
ENV MARIADB_VERSION=11.8.5
# Mon, 17 Nov 2025 18:07:34 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Mon, 17 Nov 2025 18:07:34 GMT
VOLUME [/var/lib/mysql]
# Mon, 17 Nov 2025 18:07:35 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 17 Nov 2025 18:07:35 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 17 Nov 2025 18:07:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Nov 2025 18:07:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Nov 2025 18:07:36 GMT
USER mysql
# Mon, 17 Nov 2025 18:07:36 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 17 Nov 2025 18:07:36 GMT
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
	-	`sha256:7263b3c74f6f4ec97a33caea9fe8916ed79df1f24f4fb3f156866657a0b369af`  
		Last Modified: Mon, 17 Nov 2025 18:08:55 GMT  
		Size: 125.7 MB (125721999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124332eea6fb98067bef5682105049197b03217fc6e677aa20c7ae9b0dd9a68f`  
		Last Modified: Mon, 17 Nov 2025 18:08:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30bb5f8c074565148d3b40e21237b180ccb961fea5964bba17b26c1e308ff97`  
		Last Modified: Mon, 17 Nov 2025 18:08:36 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249a3fb051274f5b80c9c0bf7498e419b79bac2b1069b4093cfd853d2885ade9`  
		Last Modified: Mon, 17 Nov 2025 18:08:37 GMT  
		Size: 8.4 KB (8394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:fd7ff1afb998b2985c9bea24daffec78156034172e6e90045af622ad0925405b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4759495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996878a856e16081e58bcef436171e2abc36e91dd414e3d32e7ab302fa260dd1`

```dockerfile
```

-	Layers:
	-	`sha256:876f8df01f0806564af1747a03c66eab90e75bcfb82e0ffadfca16d09f5b89e9`  
		Last Modified: Mon, 17 Nov 2025 19:36:14 GMT  
		Size: 4.7 MB (4724998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e4677c9b53350c8c463c0e0784a928b9f4144bdd93e2f4527eaafb1aa8dc3ae`  
		Last Modified: Mon, 17 Nov 2025 19:36:15 GMT  
		Size: 34.5 KB (34497 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:dafad1f0c3b3d19e0d7db138ad5559072aedb43ffafd8edd045c78f252b6cb54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164957119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e1649422af6079fdc29ffa5c3cc9f5e1480f1286daa7e3ac7fbecce901c29d`
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
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.5 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Fri, 14 Nov 2025 01:41:55 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Nov 2025 01:41:55 GMT
ARG MARIADB_VERSION=11.8.5
# Fri, 14 Nov 2025 01:41:55 GMT
ENV MARIADB_VERSION=11.8.5
# Mon, 17 Nov 2025 18:07:03 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Mon, 17 Nov 2025 18:07:03 GMT
VOLUME [/var/lib/mysql]
# Mon, 17 Nov 2025 18:07:03 GMT
# ARGS: MARIADB_VERSION=11.8.5
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 17 Nov 2025 18:07:03 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 17 Nov 2025 18:07:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Nov 2025 18:07:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Nov 2025 18:07:03 GMT
USER mysql
# Mon, 17 Nov 2025 18:07:03 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 17 Nov 2025 18:07:03 GMT
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
	-	`sha256:e3993ead97973778a18294b715d58b5647d3ce81345c5bc19a689db1cee0c69a`  
		Last Modified: Mon, 17 Nov 2025 18:08:14 GMT  
		Size: 118.7 MB (118651326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b1165a9dbfbf0d9f1ab022810dacec408c31cfbb1f700016664b6922aa8159`  
		Last Modified: Mon, 17 Nov 2025 18:08:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5f25456b5eb570cad34f6335092f5fcc09537c0380d3e223fc86484b7a528f`  
		Last Modified: Mon, 17 Nov 2025 18:08:03 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f78736a69dae7fb09606c3e420671403a9e7545a4844f22ad231cdd581419a`  
		Last Modified: Mon, 17 Nov 2025 18:08:03 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:0532b8324be7cabccda24d222ba88a8b6a3ee200f372ab7f777fcad14b8e07bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4753845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4269aec02f81eebe8053ed1e6a5cf5802b1b4b1dbd0479b7d5f0d45494568a`

```dockerfile
```

-	Layers:
	-	`sha256:12d7be8698043c298719403ab83ed2617ad13e77c577457444fc79fda636412b`  
		Last Modified: Mon, 17 Nov 2025 19:36:21 GMT  
		Size: 4.7 MB (4719418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddef56e01aae4141cdbcd73f8f5778512e72abfd107d0918354642c66213918c`  
		Last Modified: Mon, 17 Nov 2025 19:36:22 GMT  
		Size: 34.4 KB (34427 bytes)  
		MIME: application/vnd.in-toto+json
