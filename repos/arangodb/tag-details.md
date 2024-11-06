<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.12`](#arangodb31112)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.3`](#arangodb3123)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:db94d357494e828e21f483d367cb1ad74905acaa2c4bf14069d20816c2a8aecc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:099c257072ac9a477370ffd2f0df549886f802469a77e879de827a761cabb143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199146593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c538d9fa6a3640e85bc2a50215d85004afa6c2fce1f15060542834ffaf0516cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:24 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 06 Sep 2024 22:20:25 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 09:31:11 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 06 Nov 2024 09:31:11 GMT
ENV ARANGO_VERSION=3.11.12
# Wed, 06 Nov 2024 09:31:11 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 06 Nov 2024 09:31:11 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 06 Nov 2024 09:31:11 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Nov 2024 09:31:11 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 06 Nov 2024 09:31:11 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac9728fa40d5069156fd9415894924330f174c7f126b68efda1157a7a5b4d53`  
		Last Modified: Wed, 06 Nov 2024 19:12:53 GMT  
		Size: 195.8 MB (195751918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcb0208796e3f03fb0ef49cf1e3e1e3cceb58f251afe9cd8c70ec2f29a5664c`  
		Last Modified: Wed, 06 Nov 2024 19:12:47 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549bb6f2599cfc6738848f62e990d1d6fe8d73cc8f0a46e512e81549ff0effef`  
		Last Modified: Wed, 06 Nov 2024 19:12:47 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeec801377336a4439776f107df302f308cb74d0bb5ec515ba399c4a3754036`  
		Last Modified: Wed, 06 Nov 2024 19:12:48 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:ef8a16c965eacb7c334cd7abeed710580872a55f53a3d720447dff97a9d52bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1038006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c929d2a9a5b631c47de5ee467980b1b978506d89105e18ad02730bc0d8920c1`

```dockerfile
```

-	Layers:
	-	`sha256:180e2cce0ddcd5aa543f8e8b31cf579c277c9d811eea1ff071bce7ca6dcd15e7`  
		Last Modified: Wed, 06 Nov 2024 19:12:48 GMT  
		Size: 1.0 MB (1022379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15812a157698b9a6e3906627740a5380bda3a09168292ea380ab68eeb6c8d5c7`  
		Last Modified: Wed, 06 Nov 2024 19:12:47 GMT  
		Size: 15.6 KB (15627 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:4053e2e951bd4c72b1ea8abd3da29d5fc64e7e9b7bd62f5e0e8686e0a4d65968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202448547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac1c2b6958a02cf31e07bdaa86dda80c2820fa6a0074e963a4f9841083380f4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:24 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Fri, 06 Sep 2024 22:44:24 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 09:31:11 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 06 Nov 2024 09:31:11 GMT
ENV ARANGO_VERSION=3.11.12
# Wed, 06 Nov 2024 09:31:11 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 06 Nov 2024 09:31:11 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 06 Nov 2024 09:31:11 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Nov 2024 09:31:11 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 06 Nov 2024 09:31:11 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091552f26185110902700bce2dcb68356bb21956584ce515d1c7611cd391db8b`  
		Last Modified: Wed, 06 Nov 2024 19:12:24 GMT  
		Size: 199.2 MB (199170990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a6258db4bffac3a167f8923da4b5418befcbb17262919f845448cee3ec551e`  
		Last Modified: Wed, 06 Nov 2024 19:12:19 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279feaa2950198f993a6dd21dc4d7b028e86514221ec9591e9b9da48f1ef01e`  
		Last Modified: Wed, 06 Nov 2024 19:12:19 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29da54d6851908984b7236eb4d7ee75dc1b2cddc9c5506c3f1123c44c3c8aef2`  
		Last Modified: Wed, 06 Nov 2024 19:12:19 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:593c2b7a17a8bba84e2f4ada113a2cc8df3d1a839c1bc8cf3ae10d9e4d18a3f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1143382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6211a39c8bfa9304b923ab11b4cf25b4a4ba20fadb12e8da458436ce49e5d31`

```dockerfile
```

-	Layers:
	-	`sha256:21528cbd5a575582fdc0e50ce7aa4099559c6e3c32580a46ef70d7bdede9a311`  
		Last Modified: Wed, 06 Nov 2024 19:12:20 GMT  
		Size: 1.1 MB (1127666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eff80884679aa9303ae329c4ec00f81b8c6e0d5571ec832cd629a77038d41ef1`  
		Last Modified: Wed, 06 Nov 2024 19:12:19 GMT  
		Size: 15.7 KB (15716 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.11.12`

```console
$ docker pull arangodb@sha256:db94d357494e828e21f483d367cb1ad74905acaa2c4bf14069d20816c2a8aecc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11.12` - linux; amd64

```console
$ docker pull arangodb@sha256:099c257072ac9a477370ffd2f0df549886f802469a77e879de827a761cabb143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199146593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c538d9fa6a3640e85bc2a50215d85004afa6c2fce1f15060542834ffaf0516cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:24 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 06 Sep 2024 22:20:25 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 09:31:11 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 06 Nov 2024 09:31:11 GMT
ENV ARANGO_VERSION=3.11.12
# Wed, 06 Nov 2024 09:31:11 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 06 Nov 2024 09:31:11 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 06 Nov 2024 09:31:11 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Nov 2024 09:31:11 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 06 Nov 2024 09:31:11 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac9728fa40d5069156fd9415894924330f174c7f126b68efda1157a7a5b4d53`  
		Last Modified: Wed, 06 Nov 2024 19:12:53 GMT  
		Size: 195.8 MB (195751918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcb0208796e3f03fb0ef49cf1e3e1e3cceb58f251afe9cd8c70ec2f29a5664c`  
		Last Modified: Wed, 06 Nov 2024 19:12:47 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549bb6f2599cfc6738848f62e990d1d6fe8d73cc8f0a46e512e81549ff0effef`  
		Last Modified: Wed, 06 Nov 2024 19:12:47 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeec801377336a4439776f107df302f308cb74d0bb5ec515ba399c4a3754036`  
		Last Modified: Wed, 06 Nov 2024 19:12:48 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:ef8a16c965eacb7c334cd7abeed710580872a55f53a3d720447dff97a9d52bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1038006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c929d2a9a5b631c47de5ee467980b1b978506d89105e18ad02730bc0d8920c1`

```dockerfile
```

-	Layers:
	-	`sha256:180e2cce0ddcd5aa543f8e8b31cf579c277c9d811eea1ff071bce7ca6dcd15e7`  
		Last Modified: Wed, 06 Nov 2024 19:12:48 GMT  
		Size: 1.0 MB (1022379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15812a157698b9a6e3906627740a5380bda3a09168292ea380ab68eeb6c8d5c7`  
		Last Modified: Wed, 06 Nov 2024 19:12:47 GMT  
		Size: 15.6 KB (15627 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:4053e2e951bd4c72b1ea8abd3da29d5fc64e7e9b7bd62f5e0e8686e0a4d65968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202448547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac1c2b6958a02cf31e07bdaa86dda80c2820fa6a0074e963a4f9841083380f4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:24 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Fri, 06 Sep 2024 22:44:24 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 09:31:11 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 06 Nov 2024 09:31:11 GMT
ENV ARANGO_VERSION=3.11.12
# Wed, 06 Nov 2024 09:31:11 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 06 Nov 2024 09:31:11 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 06 Nov 2024 09:31:11 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Nov 2024 09:31:11 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 06 Nov 2024 09:31:11 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091552f26185110902700bce2dcb68356bb21956584ce515d1c7611cd391db8b`  
		Last Modified: Wed, 06 Nov 2024 19:12:24 GMT  
		Size: 199.2 MB (199170990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a6258db4bffac3a167f8923da4b5418befcbb17262919f845448cee3ec551e`  
		Last Modified: Wed, 06 Nov 2024 19:12:19 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279feaa2950198f993a6dd21dc4d7b028e86514221ec9591e9b9da48f1ef01e`  
		Last Modified: Wed, 06 Nov 2024 19:12:19 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29da54d6851908984b7236eb4d7ee75dc1b2cddc9c5506c3f1123c44c3c8aef2`  
		Last Modified: Wed, 06 Nov 2024 19:12:19 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:593c2b7a17a8bba84e2f4ada113a2cc8df3d1a839c1bc8cf3ae10d9e4d18a3f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1143382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6211a39c8bfa9304b923ab11b4cf25b4a4ba20fadb12e8da458436ce49e5d31`

```dockerfile
```

-	Layers:
	-	`sha256:21528cbd5a575582fdc0e50ce7aa4099559c6e3c32580a46ef70d7bdede9a311`  
		Last Modified: Wed, 06 Nov 2024 19:12:20 GMT  
		Size: 1.1 MB (1127666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eff80884679aa9303ae329c4ec00f81b8c6e0d5571ec832cd629a77038d41ef1`  
		Last Modified: Wed, 06 Nov 2024 19:12:19 GMT  
		Size: 15.7 KB (15716 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:2c70fa28ca16f2a958f8fda1fb2726ed98200927cd0b0001959aa6334f800126
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:89340f375a9d6c32d705d21e2274dfb7da380f5159f29d194d8d7bfa5fb75ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304636048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a18220975714af4ed2799438fdd8bb06d6f9c79d142c955d959e3a2b33a2f37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:24 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 06 Sep 2024 22:20:25 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 30 Oct 2024 15:12:33 GMT
ENV ARANGO_VERSION=3.12.3
# Wed, 30 Oct 2024 15:12:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 30 Oct 2024 15:12:33 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 30 Oct 2024 15:12:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 30 Oct 2024 15:12:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd3bcbd2d9fd875fd9b05d65ca35599a4ed798eb90f7687b9f5759cbca27cc7`  
		Last Modified: Wed, 30 Oct 2024 18:01:34 GMT  
		Size: 301.2 MB (301241699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1b2be9d203681807a5173705139c3aba7aa6c65020d1becbd8441a628d52d8`  
		Last Modified: Wed, 30 Oct 2024 18:01:27 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d3890997c4513e11dc47ab3c278bddbe7665890dccdee12771728de4a379fb`  
		Last Modified: Wed, 30 Oct 2024 18:01:27 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:f0bb1a139fab82268f07571416ef01aabb8110b530e034d3ed42412dbdd30295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.7 KB (372706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a2cb90e275f2a98d551cf2abf8c610328d43feca89da32d9cf6e1839b29508`

```dockerfile
```

-	Layers:
	-	`sha256:5d33d348645e5c8ad03455b3777e090e20402167f3d11af423cb899ea77fcbaa`  
		Last Modified: Wed, 30 Oct 2024 18:01:27 GMT  
		Size: 358.5 KB (358520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50310f41b925e3f06ecab10e53f330cec2afea806ffe7367b3be1c099cc7421b`  
		Last Modified: Wed, 30 Oct 2024 18:01:27 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:d0e4ba04417cb3503650238461aa15a5dbd695a085f1271467e2de8708648f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306524554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7370f71294866113289693b26e6166b6947769ff624e5f25c1d581d42396e27a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:24 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Fri, 06 Sep 2024 22:44:24 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 30 Oct 2024 15:12:33 GMT
ENV ARANGO_VERSION=3.12.3
# Wed, 30 Oct 2024 15:12:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 30 Oct 2024 15:12:33 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 30 Oct 2024 15:12:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 30 Oct 2024 15:12:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7083aa2dfc67dc21b5ce6762f15f645b95a0f5407ef14ab3d52883cae8e706cd`  
		Last Modified: Wed, 30 Oct 2024 18:01:13 GMT  
		Size: 303.2 MB (303247329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3aea7875c62355ba8d015dbc6f06e21331ef909a86a46091926d9f4b34cf48`  
		Last Modified: Wed, 30 Oct 2024 18:01:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9878675c62bb1785462bb8b9510f20543bd6655fb1cfa0a43eae892ebe2e02`  
		Last Modified: Wed, 30 Oct 2024 18:01:05 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:1e2263466f7af665c50b0d2683c82623f7fd3afa00647ada61ec8ea1a3fc47c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.1 KB (478106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6e47fdce3ee50762f1ea3445227641daaecef73bb1a9104f5f69459061aef1`

```dockerfile
```

-	Layers:
	-	`sha256:6703001d32d225e56b582aa77c6bc6c9037645a675ba32e064d6e98bf6103198`  
		Last Modified: Wed, 30 Oct 2024 18:01:06 GMT  
		Size: 463.8 KB (463819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cfd1d76176849ac3e8ac0052b60e930ad16fd1d486b2d5a34fd6fafeb95f9ee`  
		Last Modified: Wed, 30 Oct 2024 18:01:05 GMT  
		Size: 14.3 KB (14287 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.3`

```console
$ docker pull arangodb@sha256:2c70fa28ca16f2a958f8fda1fb2726ed98200927cd0b0001959aa6334f800126
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12.3` - linux; amd64

```console
$ docker pull arangodb@sha256:89340f375a9d6c32d705d21e2274dfb7da380f5159f29d194d8d7bfa5fb75ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304636048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a18220975714af4ed2799438fdd8bb06d6f9c79d142c955d959e3a2b33a2f37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:24 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 06 Sep 2024 22:20:25 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 30 Oct 2024 15:12:33 GMT
ENV ARANGO_VERSION=3.12.3
# Wed, 30 Oct 2024 15:12:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 30 Oct 2024 15:12:33 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 30 Oct 2024 15:12:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 30 Oct 2024 15:12:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd3bcbd2d9fd875fd9b05d65ca35599a4ed798eb90f7687b9f5759cbca27cc7`  
		Last Modified: Wed, 30 Oct 2024 18:01:34 GMT  
		Size: 301.2 MB (301241699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1b2be9d203681807a5173705139c3aba7aa6c65020d1becbd8441a628d52d8`  
		Last Modified: Wed, 30 Oct 2024 18:01:27 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d3890997c4513e11dc47ab3c278bddbe7665890dccdee12771728de4a379fb`  
		Last Modified: Wed, 30 Oct 2024 18:01:27 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.3` - unknown; unknown

```console
$ docker pull arangodb@sha256:f0bb1a139fab82268f07571416ef01aabb8110b530e034d3ed42412dbdd30295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.7 KB (372706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a2cb90e275f2a98d551cf2abf8c610328d43feca89da32d9cf6e1839b29508`

```dockerfile
```

-	Layers:
	-	`sha256:5d33d348645e5c8ad03455b3777e090e20402167f3d11af423cb899ea77fcbaa`  
		Last Modified: Wed, 30 Oct 2024 18:01:27 GMT  
		Size: 358.5 KB (358520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50310f41b925e3f06ecab10e53f330cec2afea806ffe7367b3be1c099cc7421b`  
		Last Modified: Wed, 30 Oct 2024 18:01:27 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12.3` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:d0e4ba04417cb3503650238461aa15a5dbd695a085f1271467e2de8708648f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306524554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7370f71294866113289693b26e6166b6947769ff624e5f25c1d581d42396e27a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:24 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Fri, 06 Sep 2024 22:44:24 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 30 Oct 2024 15:12:33 GMT
ENV ARANGO_VERSION=3.12.3
# Wed, 30 Oct 2024 15:12:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 30 Oct 2024 15:12:33 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 30 Oct 2024 15:12:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 30 Oct 2024 15:12:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7083aa2dfc67dc21b5ce6762f15f645b95a0f5407ef14ab3d52883cae8e706cd`  
		Last Modified: Wed, 30 Oct 2024 18:01:13 GMT  
		Size: 303.2 MB (303247329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3aea7875c62355ba8d015dbc6f06e21331ef909a86a46091926d9f4b34cf48`  
		Last Modified: Wed, 30 Oct 2024 18:01:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9878675c62bb1785462bb8b9510f20543bd6655fb1cfa0a43eae892ebe2e02`  
		Last Modified: Wed, 30 Oct 2024 18:01:05 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.3` - unknown; unknown

```console
$ docker pull arangodb@sha256:1e2263466f7af665c50b0d2683c82623f7fd3afa00647ada61ec8ea1a3fc47c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.1 KB (478106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6e47fdce3ee50762f1ea3445227641daaecef73bb1a9104f5f69459061aef1`

```dockerfile
```

-	Layers:
	-	`sha256:6703001d32d225e56b582aa77c6bc6c9037645a675ba32e064d6e98bf6103198`  
		Last Modified: Wed, 30 Oct 2024 18:01:06 GMT  
		Size: 463.8 KB (463819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cfd1d76176849ac3e8ac0052b60e930ad16fd1d486b2d5a34fd6fafeb95f9ee`  
		Last Modified: Wed, 30 Oct 2024 18:01:05 GMT  
		Size: 14.3 KB (14287 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:2c70fa28ca16f2a958f8fda1fb2726ed98200927cd0b0001959aa6334f800126
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:89340f375a9d6c32d705d21e2274dfb7da380f5159f29d194d8d7bfa5fb75ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304636048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a18220975714af4ed2799438fdd8bb06d6f9c79d142c955d959e3a2b33a2f37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:24 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 06 Sep 2024 22:20:25 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 30 Oct 2024 15:12:33 GMT
ENV ARANGO_VERSION=3.12.3
# Wed, 30 Oct 2024 15:12:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 30 Oct 2024 15:12:33 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 30 Oct 2024 15:12:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 30 Oct 2024 15:12:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd3bcbd2d9fd875fd9b05d65ca35599a4ed798eb90f7687b9f5759cbca27cc7`  
		Last Modified: Wed, 30 Oct 2024 18:01:34 GMT  
		Size: 301.2 MB (301241699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1b2be9d203681807a5173705139c3aba7aa6c65020d1becbd8441a628d52d8`  
		Last Modified: Wed, 30 Oct 2024 18:01:27 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d3890997c4513e11dc47ab3c278bddbe7665890dccdee12771728de4a379fb`  
		Last Modified: Wed, 30 Oct 2024 18:01:27 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:f0bb1a139fab82268f07571416ef01aabb8110b530e034d3ed42412dbdd30295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.7 KB (372706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a2cb90e275f2a98d551cf2abf8c610328d43feca89da32d9cf6e1839b29508`

```dockerfile
```

-	Layers:
	-	`sha256:5d33d348645e5c8ad03455b3777e090e20402167f3d11af423cb899ea77fcbaa`  
		Last Modified: Wed, 30 Oct 2024 18:01:27 GMT  
		Size: 358.5 KB (358520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50310f41b925e3f06ecab10e53f330cec2afea806ffe7367b3be1c099cc7421b`  
		Last Modified: Wed, 30 Oct 2024 18:01:27 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:d0e4ba04417cb3503650238461aa15a5dbd695a085f1271467e2de8708648f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306524554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7370f71294866113289693b26e6166b6947769ff624e5f25c1d581d42396e27a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:24 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Fri, 06 Sep 2024 22:44:24 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 30 Oct 2024 15:12:33 GMT
ENV ARANGO_VERSION=3.12.3
# Wed, 30 Oct 2024 15:12:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 30 Oct 2024 15:12:33 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 30 Oct 2024 15:12:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 30 Oct 2024 15:12:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7083aa2dfc67dc21b5ce6762f15f645b95a0f5407ef14ab3d52883cae8e706cd`  
		Last Modified: Wed, 30 Oct 2024 18:01:13 GMT  
		Size: 303.2 MB (303247329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3aea7875c62355ba8d015dbc6f06e21331ef909a86a46091926d9f4b34cf48`  
		Last Modified: Wed, 30 Oct 2024 18:01:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9878675c62bb1785462bb8b9510f20543bd6655fb1cfa0a43eae892ebe2e02`  
		Last Modified: Wed, 30 Oct 2024 18:01:05 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:1e2263466f7af665c50b0d2683c82623f7fd3afa00647ada61ec8ea1a3fc47c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.1 KB (478106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6e47fdce3ee50762f1ea3445227641daaecef73bb1a9104f5f69459061aef1`

```dockerfile
```

-	Layers:
	-	`sha256:6703001d32d225e56b582aa77c6bc6c9037645a675ba32e064d6e98bf6103198`  
		Last Modified: Wed, 30 Oct 2024 18:01:06 GMT  
		Size: 463.8 KB (463819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cfd1d76176849ac3e8ac0052b60e930ad16fd1d486b2d5a34fd6fafeb95f9ee`  
		Last Modified: Wed, 30 Oct 2024 18:01:05 GMT  
		Size: 14.3 KB (14287 bytes)  
		MIME: application/vnd.in-toto+json
