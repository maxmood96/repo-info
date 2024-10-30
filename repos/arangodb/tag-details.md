<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.11`](#arangodb31111)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.3`](#arangodb3123)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:2ccdaad9829530013523e1227a4a615f790d7838aa00b95417911d6a13e0c661
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:1c310e96a29579392e38654e75336cc644c9f4e0ca10c99d606e7a4687bc7234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 MB (199037949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6dad09564c05c4d5060b737af7ac849e84c439b03f4fb2505ad196be29f739`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:24 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 06 Sep 2024 22:20:25 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 14:19:55 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 10 Sep 2024 14:19:55 GMT
ENV ARANGO_VERSION=3.11.11
# Tue, 10 Sep 2024 14:19:55 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Tue, 10 Sep 2024 14:19:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 10 Sep 2024 14:19:55 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Tue, 10 Sep 2024 14:19:55 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 10 Sep 2024 14:19:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 10 Sep 2024 14:19:55 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Tue, 10 Sep 2024 14:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Sep 2024 14:19:55 GMT
EXPOSE map[8529/tcp:{}]
# Tue, 10 Sep 2024 14:19:55 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2cdd11b8b7a8f27850730a3c7537c0ca2cfc93fd53a3f8a81e45121ac6bbe8`  
		Last Modified: Tue, 10 Sep 2024 21:57:53 GMT  
		Size: 195.6 MB (195643272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1992c0b7389b641fb5f180dc214cfdfb618db85de461b61e9fe6daf0d35f93e`  
		Last Modified: Tue, 10 Sep 2024 21:57:51 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755547b3e194c65dce46edd6af5218bd37278ea2b014c4952f268a08fdaf5d1a`  
		Last Modified: Tue, 10 Sep 2024 21:57:51 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e17249fb35e28905b5033abd4407f2d84a21a770a4f1e1bf0237f88a3a03f2`  
		Last Modified: Tue, 10 Sep 2024 21:57:51 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:2895e862578a80d42934b8529fe52adbef407815c78f846404aed46b6577fbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **965.6 KB (965563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a734e7ccda9076e9edbabb308fa09cbaa9f9c5634d5beb60eacc73d9036b7ad9`

```dockerfile
```

-	Layers:
	-	`sha256:5e62294fd60618272cf488640256ef41ff59e01e335a7b719fc9c23a6f0b7d5d`  
		Last Modified: Tue, 10 Sep 2024 21:57:51 GMT  
		Size: 950.0 KB (949970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1a15d80c3f2e7ef07b10ecf13a6fb2041eca9f381ba5a269d3f4cedcee5a1e`  
		Last Modified: Tue, 10 Sep 2024 21:57:51 GMT  
		Size: 15.6 KB (15593 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:3f36bd811fb4ef87df55dbc0526940147a9902cdb9945060f29e6166c1e0dd2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202355675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2239437791e8f136918c4c85929e25a5f1c3ca7a708aae1b0bdd932e454452e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:24 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Fri, 06 Sep 2024 22:44:24 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 14:19:55 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 10 Sep 2024 14:19:55 GMT
ENV ARANGO_VERSION=3.11.11
# Tue, 10 Sep 2024 14:19:55 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Tue, 10 Sep 2024 14:19:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 10 Sep 2024 14:19:55 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Tue, 10 Sep 2024 14:19:55 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 10 Sep 2024 14:19:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 10 Sep 2024 14:19:55 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Tue, 10 Sep 2024 14:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Sep 2024 14:19:55 GMT
EXPOSE map[8529/tcp:{}]
# Tue, 10 Sep 2024 14:19:55 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea5c7bea24290b6b8c065ac658256f0560f75bb453eba2d78761e71d4e74b36`  
		Last Modified: Tue, 10 Sep 2024 21:57:48 GMT  
		Size: 199.1 MB (199078122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cbd8f7f1d9e2ad252542fe305c35474f80eb70a9414964a52426f2ab9f084c`  
		Last Modified: Tue, 10 Sep 2024 21:57:43 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ac93a82425b82be56c268f572636040ea3733b8ab80b28364e1d0b67dfc7d1`  
		Last Modified: Tue, 10 Sep 2024 21:57:43 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e46479d1792ff39d8e6ac7268b8267f9efbd3e92b809b4db08e04bd09289a5`  
		Last Modified: Tue, 10 Sep 2024 21:57:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:7747a7a56bd80d3f485ebafa4527b8d8d3e76041b2c3bdb568ea52dacd8ac5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1071126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0588269341e3b2aba7c6d3912ed7b9c72bda0b7dc935e3f19980b05176d7a6`

```dockerfile
```

-	Layers:
	-	`sha256:75c714c16f055ff453d6d1418de4a476b8c93eb2a14fca5d6e12c4f90b117103`  
		Last Modified: Tue, 10 Sep 2024 21:57:44 GMT  
		Size: 1.1 MB (1055257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4ba76d8b9538b62ef4b80e7cf75fd5bc6a2d736cf3703f308a35f6334759a8f`  
		Last Modified: Tue, 10 Sep 2024 21:57:43 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.11.11`

```console
$ docker pull arangodb@sha256:2ccdaad9829530013523e1227a4a615f790d7838aa00b95417911d6a13e0c661
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11.11` - linux; amd64

```console
$ docker pull arangodb@sha256:1c310e96a29579392e38654e75336cc644c9f4e0ca10c99d606e7a4687bc7234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 MB (199037949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6dad09564c05c4d5060b737af7ac849e84c439b03f4fb2505ad196be29f739`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:24 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 06 Sep 2024 22:20:25 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 14:19:55 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 10 Sep 2024 14:19:55 GMT
ENV ARANGO_VERSION=3.11.11
# Tue, 10 Sep 2024 14:19:55 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Tue, 10 Sep 2024 14:19:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 10 Sep 2024 14:19:55 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Tue, 10 Sep 2024 14:19:55 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 10 Sep 2024 14:19:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 10 Sep 2024 14:19:55 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Tue, 10 Sep 2024 14:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Sep 2024 14:19:55 GMT
EXPOSE map[8529/tcp:{}]
# Tue, 10 Sep 2024 14:19:55 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2cdd11b8b7a8f27850730a3c7537c0ca2cfc93fd53a3f8a81e45121ac6bbe8`  
		Last Modified: Tue, 10 Sep 2024 21:57:53 GMT  
		Size: 195.6 MB (195643272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1992c0b7389b641fb5f180dc214cfdfb618db85de461b61e9fe6daf0d35f93e`  
		Last Modified: Tue, 10 Sep 2024 21:57:51 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755547b3e194c65dce46edd6af5218bd37278ea2b014c4952f268a08fdaf5d1a`  
		Last Modified: Tue, 10 Sep 2024 21:57:51 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e17249fb35e28905b5033abd4407f2d84a21a770a4f1e1bf0237f88a3a03f2`  
		Last Modified: Tue, 10 Sep 2024 21:57:51 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:2895e862578a80d42934b8529fe52adbef407815c78f846404aed46b6577fbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **965.6 KB (965563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a734e7ccda9076e9edbabb308fa09cbaa9f9c5634d5beb60eacc73d9036b7ad9`

```dockerfile
```

-	Layers:
	-	`sha256:5e62294fd60618272cf488640256ef41ff59e01e335a7b719fc9c23a6f0b7d5d`  
		Last Modified: Tue, 10 Sep 2024 21:57:51 GMT  
		Size: 950.0 KB (949970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1a15d80c3f2e7ef07b10ecf13a6fb2041eca9f381ba5a269d3f4cedcee5a1e`  
		Last Modified: Tue, 10 Sep 2024 21:57:51 GMT  
		Size: 15.6 KB (15593 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:3f36bd811fb4ef87df55dbc0526940147a9902cdb9945060f29e6166c1e0dd2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202355675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2239437791e8f136918c4c85929e25a5f1c3ca7a708aae1b0bdd932e454452e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:24 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Fri, 06 Sep 2024 22:44:24 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 14:19:55 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 10 Sep 2024 14:19:55 GMT
ENV ARANGO_VERSION=3.11.11
# Tue, 10 Sep 2024 14:19:55 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Tue, 10 Sep 2024 14:19:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 10 Sep 2024 14:19:55 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Tue, 10 Sep 2024 14:19:55 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 10 Sep 2024 14:19:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 10 Sep 2024 14:19:55 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Tue, 10 Sep 2024 14:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Sep 2024 14:19:55 GMT
EXPOSE map[8529/tcp:{}]
# Tue, 10 Sep 2024 14:19:55 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea5c7bea24290b6b8c065ac658256f0560f75bb453eba2d78761e71d4e74b36`  
		Last Modified: Tue, 10 Sep 2024 21:57:48 GMT  
		Size: 199.1 MB (199078122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cbd8f7f1d9e2ad252542fe305c35474f80eb70a9414964a52426f2ab9f084c`  
		Last Modified: Tue, 10 Sep 2024 21:57:43 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ac93a82425b82be56c268f572636040ea3733b8ab80b28364e1d0b67dfc7d1`  
		Last Modified: Tue, 10 Sep 2024 21:57:43 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e46479d1792ff39d8e6ac7268b8267f9efbd3e92b809b4db08e04bd09289a5`  
		Last Modified: Tue, 10 Sep 2024 21:57:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:7747a7a56bd80d3f485ebafa4527b8d8d3e76041b2c3bdb568ea52dacd8ac5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1071126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0588269341e3b2aba7c6d3912ed7b9c72bda0b7dc935e3f19980b05176d7a6`

```dockerfile
```

-	Layers:
	-	`sha256:75c714c16f055ff453d6d1418de4a476b8c93eb2a14fca5d6e12c4f90b117103`  
		Last Modified: Tue, 10 Sep 2024 21:57:44 GMT  
		Size: 1.1 MB (1055257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4ba76d8b9538b62ef4b80e7cf75fd5bc6a2d736cf3703f308a35f6334759a8f`  
		Last Modified: Tue, 10 Sep 2024 21:57:43 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:86900a367435d28e68c5ea023f074887f446a2a0c31d4eae3d7812ef9bc4f6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:1116070d437ec3d4bc57691d52ce1bfee8496a8bb34d0c73c19896bed0fbc3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302882938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b065f7e6170743361c0924f465c62f3ab5a536eed80b27ed0ce07dd4deeebd2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 27 Aug 2024 15:12:16 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 27 Aug 2024 15:12:16 GMT
ENV ARANGO_VERSION=3.12.2
# Tue, 27 Aug 2024 15:12:16 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 27 Aug 2024 15:12:16 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 27 Aug 2024 15:12:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
EXPOSE map[8529/tcp:{}]
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a1f452304f4c30119e5711de9c5cde32028436b3418d3fdac26994d21194b7`  
		Last Modified: Fri, 06 Sep 2024 23:15:34 GMT  
		Size: 299.5 MB (299488588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf357aa9fa450477bae167fd108ff01273d3c63731898bf1d79ffdd23aec29e`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbf4ac60298128ae88a19a2838044a9bedc05191c90540ca3112ac02b44d6e9`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:6e8cb3815727ccb200f4f86f85fca645479e7071f469a9bcb2f5e6933b79d57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.5 KB (361542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b49375ad3fd2b5c90a7b49f4fd7c148e5ca0810ebad955d54d8e16cd83a340`

```dockerfile
```

-	Layers:
	-	`sha256:48331eb50787bc4daa1e60cc3a5e848a12b33de2a440e3de6228a8a4f58f9040`  
		Last Modified: Fri, 06 Sep 2024 23:15:31 GMT  
		Size: 347.4 KB (347390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa77f4a14b212ced8573b6fa04b43f9c086d0fb680f06bb38177a859c4b40150`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 14.2 KB (14152 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:0dc3cc2632158e7292309629cf33b0401c6901b53f8c633c06133f0cc8a0c3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 MB (304675738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42fd3351c3ef519fbec5a4ec501809ba8e52dea42b4f728222bf8e1c096b6a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 27 Aug 2024 15:12:16 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 27 Aug 2024 15:12:16 GMT
ENV ARANGO_VERSION=3.12.2
# Tue, 27 Aug 2024 15:12:16 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 27 Aug 2024 15:12:16 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 27 Aug 2024 15:12:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
EXPOSE map[8529/tcp:{}]
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf7966d79f14a85391123be39cca32586ba4f7500728c5daeca5fdb623b0e8d`  
		Last Modified: Sat, 07 Sep 2024 04:18:35 GMT  
		Size: 301.4 MB (301398510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f8fcaf4551340a01b8982880a08d0cbde8e6e66b15ba167b26543a9c697445`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5249cc2ab632e58d18be46e53425e146cfe0d2ad0ef378241ee586f5552f64d`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:195e356b696c821ab8e39b50c622f7c1be703b4ce8efa13bf578555c6362c534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.1 KB (467129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714bbca94d370022c14f72fde61686228c0839192ff117db2e654be54787271a`

```dockerfile
```

-	Layers:
	-	`sha256:32dea479efdcee2e8752a57510dcd823c08ad9889dade0e9d7f1e9d249ce82ab`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 452.7 KB (452689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65765fe83c5b07f248b8cd5b8daa3876c3b97584729483428f2a3b819e5eab54`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 14.4 KB (14440 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.3`

**does not exist** (yet?)

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:86900a367435d28e68c5ea023f074887f446a2a0c31d4eae3d7812ef9bc4f6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:1116070d437ec3d4bc57691d52ce1bfee8496a8bb34d0c73c19896bed0fbc3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302882938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b065f7e6170743361c0924f465c62f3ab5a536eed80b27ed0ce07dd4deeebd2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 27 Aug 2024 15:12:16 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 27 Aug 2024 15:12:16 GMT
ENV ARANGO_VERSION=3.12.2
# Tue, 27 Aug 2024 15:12:16 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 27 Aug 2024 15:12:16 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 27 Aug 2024 15:12:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
EXPOSE map[8529/tcp:{}]
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a1f452304f4c30119e5711de9c5cde32028436b3418d3fdac26994d21194b7`  
		Last Modified: Fri, 06 Sep 2024 23:15:34 GMT  
		Size: 299.5 MB (299488588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf357aa9fa450477bae167fd108ff01273d3c63731898bf1d79ffdd23aec29e`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbf4ac60298128ae88a19a2838044a9bedc05191c90540ca3112ac02b44d6e9`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:6e8cb3815727ccb200f4f86f85fca645479e7071f469a9bcb2f5e6933b79d57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.5 KB (361542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b49375ad3fd2b5c90a7b49f4fd7c148e5ca0810ebad955d54d8e16cd83a340`

```dockerfile
```

-	Layers:
	-	`sha256:48331eb50787bc4daa1e60cc3a5e848a12b33de2a440e3de6228a8a4f58f9040`  
		Last Modified: Fri, 06 Sep 2024 23:15:31 GMT  
		Size: 347.4 KB (347390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa77f4a14b212ced8573b6fa04b43f9c086d0fb680f06bb38177a859c4b40150`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 14.2 KB (14152 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:0dc3cc2632158e7292309629cf33b0401c6901b53f8c633c06133f0cc8a0c3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 MB (304675738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42fd3351c3ef519fbec5a4ec501809ba8e52dea42b4f728222bf8e1c096b6a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 27 Aug 2024 15:12:16 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 27 Aug 2024 15:12:16 GMT
ENV ARANGO_VERSION=3.12.2
# Tue, 27 Aug 2024 15:12:16 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 27 Aug 2024 15:12:16 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 27 Aug 2024 15:12:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
EXPOSE map[8529/tcp:{}]
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf7966d79f14a85391123be39cca32586ba4f7500728c5daeca5fdb623b0e8d`  
		Last Modified: Sat, 07 Sep 2024 04:18:35 GMT  
		Size: 301.4 MB (301398510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f8fcaf4551340a01b8982880a08d0cbde8e6e66b15ba167b26543a9c697445`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5249cc2ab632e58d18be46e53425e146cfe0d2ad0ef378241ee586f5552f64d`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:195e356b696c821ab8e39b50c622f7c1be703b4ce8efa13bf578555c6362c534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.1 KB (467129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714bbca94d370022c14f72fde61686228c0839192ff117db2e654be54787271a`

```dockerfile
```

-	Layers:
	-	`sha256:32dea479efdcee2e8752a57510dcd823c08ad9889dade0e9d7f1e9d249ce82ab`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 452.7 KB (452689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65765fe83c5b07f248b8cd5b8daa3876c3b97584729483428f2a3b819e5eab54`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 14.4 KB (14440 bytes)  
		MIME: application/vnd.in-toto+json
