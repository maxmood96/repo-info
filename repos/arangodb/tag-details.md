<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.10.1`](#arangodb311101)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.0.2`](#arangodb31202)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:7888eebfedaef45cdd6eceec6dc151a55eb3244d9eee55d86c7192bc91a1bf5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:c0ca6f4f8639b205cfb58d6e3f0c0717c17caf754fa1b9855ad63db3367bd364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.8 MB (198844614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15190d1264e60de98a6bf757f664a575361b64442704cc054323f1d33cf01a8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:15 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Thu, 20 Jun 2024 20:17:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 17:12:04 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 03 Jul 2024 17:12:04 GMT
ENV ARANGO_VERSION=3.11.10
# Wed, 03 Jul 2024 17:12:04 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 03 Jul 2024 17:12:04 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 03 Jul 2024 17:12:04 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 03 Jul 2024 17:12:04 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 03 Jul 2024 17:12:04 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 03 Jul 2024 17:12:04 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Wed, 03 Jul 2024 17:12:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 17:12:04 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 03 Jul 2024 17:12:04 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c33a4cbe87975ab4d626c60605df2d2b21ccbbd72c8f64c852ba72f06d872b`  
		Last Modified: Wed, 03 Jul 2024 17:59:12 GMT  
		Size: 195.5 MB (195452166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0a5d3d97e35540499de63e36ef784608c8478a9890fe9253d779ad3c285be0`  
		Last Modified: Wed, 03 Jul 2024 17:59:08 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cf53e5d7e16eb8166105f613855e333fdbeea40acffea97f4dfaf0c1ef1051`  
		Last Modified: Wed, 03 Jul 2024 17:59:08 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b81996e84fe34e0b7ce60a9e9f93adf86aae43f405c63fc7909da743d4ae6c`  
		Last Modified: Wed, 03 Jul 2024 17:59:08 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:31d31250246466049fbaa5252c47680fe8d85036a726f213a91649db95a6d90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.6 KB (906622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b234ab32eaa8cd886159717f1523b38c0603dfbca6bba9c4262dbf939b7cfe15`

```dockerfile
```

-	Layers:
	-	`sha256:ecc924e7b111fc9e9fed30c39b5846b657d81110e1068ad12afcb29dbe504067`  
		Last Modified: Wed, 03 Jul 2024 17:59:08 GMT  
		Size: 891.0 KB (891029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac3a8e241a78d0bebf63225434052565caa4260d94bce002eace92b23d867774`  
		Last Modified: Wed, 03 Jul 2024 17:59:08 GMT  
		Size: 15.6 KB (15593 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:32099acd2decc44973fd8ad00632960be150400f6768d1d83b82b0cf2430bb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202138505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440c04204c4b9f8adda96b664c62634c49239e8b6024c98db0bc3acd508c3524`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:45 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Thu, 20 Jun 2024 17:40:45 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 17:12:04 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 03 Jul 2024 17:12:04 GMT
ENV ARANGO_VERSION=3.11.10
# Wed, 03 Jul 2024 17:12:04 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 03 Jul 2024 17:12:04 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 03 Jul 2024 17:12:04 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 03 Jul 2024 17:12:04 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 03 Jul 2024 17:12:04 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 03 Jul 2024 17:12:04 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Wed, 03 Jul 2024 17:12:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 17:12:04 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 03 Jul 2024 17:12:04 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a432d3e1299428b39385af74adf5969136f19b135d12839f1d0f65d3322765`  
		Last Modified: Wed, 03 Jul 2024 19:22:26 GMT  
		Size: 198.9 MB (198863433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e53730c09c9f56825266e21ff5dd5858355ba2a5863278240949e4c9d3d911`  
		Last Modified: Wed, 03 Jul 2024 19:22:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfb1f41d4aa76b6b566d41f168622065e3aa94a34bbf5ebb40473971c8d746f`  
		Last Modified: Wed, 03 Jul 2024 19:22:22 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83341aebacbbe91238e7477d869a5f86e33e223b662a792bc7706db220fb29cc`  
		Last Modified: Wed, 03 Jul 2024 19:22:22 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:988dedf3ef408d5a583273ac1b1a86eb2a5aa742e102be4af1fc702862860f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bcef955f3d9e0039a1b84a41ad60718a828a0821c7ed4492e32585a598331c`

```dockerfile
```

-	Layers:
	-	`sha256:92e18cde97601bebc439aa45dd0623da8c3a069a2949bcbc3c65213e6765d07e`  
		Last Modified: Wed, 03 Jul 2024 19:22:22 GMT  
		Size: 996.3 KB (996316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5de8bcec61904840aa6095708562e9c5acdbbe2b047ce9c3d7380644c823e809`  
		Last Modified: Wed, 03 Jul 2024 19:22:22 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.11.10.1`

**does not exist** (yet?)

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:f1fa8f00c87ce7baea6f03085ed2a9cc4e3509dc098e8b2f164c3f2b4866554f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:37e593cdb44146fbe64b0e404407a174df22ee9b379262d7cfb5c1e8d9f1d3f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302162975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22810e5fe7473fcd9e24ea467d0dc5984aad8196b0e3623cbcc2a2ff2df6db4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Fri, 03 May 2024 11:13:37 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 11:13:37 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 03 May 2024 11:13:37 GMT
ENV ARANGO_VERSION=3.12.0.2
# Fri, 03 May 2024 11:13:37 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 03 May 2024 11:13:37 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 03 May 2024 11:13:37 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 03 May 2024 11:13:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 May 2024 11:13:37 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 03 May 2024 11:13:37 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e27b48c8fe935e54cfe60ef3e46dd5663da75405f18ec14ca26627c4c0ec87`  
		Last Modified: Thu, 20 Jun 2024 20:55:06 GMT  
		Size: 298.8 MB (298770856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da899acd957c7dde28a69cae008d106b7d9798c02abb60bb68e929e3c61b61d`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162d83bef531a5f2661a61373aec6ef7d443a12b2d9da806265c6d695851db9c`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:126383c986a5debc5b56aee1ccf6dc3fa57b7577ed67ba73690fda69dcb08261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.9 KB (334942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee995ef825f2cfe6a628ef9d08c7e986f980253d80e7f85a75fbfaf7bcca8d54`

```dockerfile
```

-	Layers:
	-	`sha256:a3b0687d6d0d3de2777bc0f49d8351560656047f1a5fee01b3ab2aec6f348947`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 320.8 KB (320773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd4fecd31e6f68f71a9f873f644baa34aa92db09933642d69c17ee6853ee295`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 14.2 KB (14169 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:2c16164a6bcc6cd3d9a2db7b22735d444d11b280643f7246798f46ee1a06b4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304401348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b421284ca5ae90a3b49e7d898574254a6bca120654a639535efafa7c098c7076`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Fri, 03 May 2024 11:13:37 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 11:13:37 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 03 May 2024 11:13:37 GMT
ENV ARANGO_VERSION=3.12.0.2
# Fri, 03 May 2024 11:13:37 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 03 May 2024 11:13:37 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 03 May 2024 11:13:37 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 03 May 2024 11:13:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 May 2024 11:13:37 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 03 May 2024 11:13:37 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c6c464299418ea712993cb2f3c94ba89286c6e373921a08be6a506bf4e9b11`  
		Last Modified: Fri, 21 Jun 2024 01:57:28 GMT  
		Size: 301.1 MB (301126606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d363ca46bcc2fd49939bce38496b2623eb437a5da829687488a9aef0f12afe2`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4484419ad40939d2a8d59586c4c93713ac0f3280c28fcc522b370497d0e10e8d`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:9b962121ad204153e5b4779d1eaa7351b688a51a9f6b46eb0c2640124f885dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 KB (440529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8edef511ac2d4b771c1de30e3cfd542ee56f0b9f6354a23e775c4f9adef7b17`

```dockerfile
```

-	Layers:
	-	`sha256:324d5c14295aef3b00263a4d8dcac0cea131640012528e5053cd58112f15c93d`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 426.1 KB (426072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f5a4286706b8b8e91d1a476201e00cd0437499fe79291b058585463add2d374`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 14.5 KB (14457 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.0.2`

```console
$ docker pull arangodb@sha256:f1fa8f00c87ce7baea6f03085ed2a9cc4e3509dc098e8b2f164c3f2b4866554f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12.0.2` - linux; amd64

```console
$ docker pull arangodb@sha256:37e593cdb44146fbe64b0e404407a174df22ee9b379262d7cfb5c1e8d9f1d3f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302162975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22810e5fe7473fcd9e24ea467d0dc5984aad8196b0e3623cbcc2a2ff2df6db4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Fri, 03 May 2024 11:13:37 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 11:13:37 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 03 May 2024 11:13:37 GMT
ENV ARANGO_VERSION=3.12.0.2
# Fri, 03 May 2024 11:13:37 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 03 May 2024 11:13:37 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 03 May 2024 11:13:37 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 03 May 2024 11:13:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 May 2024 11:13:37 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 03 May 2024 11:13:37 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e27b48c8fe935e54cfe60ef3e46dd5663da75405f18ec14ca26627c4c0ec87`  
		Last Modified: Thu, 20 Jun 2024 20:55:06 GMT  
		Size: 298.8 MB (298770856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da899acd957c7dde28a69cae008d106b7d9798c02abb60bb68e929e3c61b61d`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162d83bef531a5f2661a61373aec6ef7d443a12b2d9da806265c6d695851db9c`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.0.2` - unknown; unknown

```console
$ docker pull arangodb@sha256:126383c986a5debc5b56aee1ccf6dc3fa57b7577ed67ba73690fda69dcb08261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.9 KB (334942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee995ef825f2cfe6a628ef9d08c7e986f980253d80e7f85a75fbfaf7bcca8d54`

```dockerfile
```

-	Layers:
	-	`sha256:a3b0687d6d0d3de2777bc0f49d8351560656047f1a5fee01b3ab2aec6f348947`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 320.8 KB (320773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd4fecd31e6f68f71a9f873f644baa34aa92db09933642d69c17ee6853ee295`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 14.2 KB (14169 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12.0.2` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:2c16164a6bcc6cd3d9a2db7b22735d444d11b280643f7246798f46ee1a06b4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304401348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b421284ca5ae90a3b49e7d898574254a6bca120654a639535efafa7c098c7076`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Fri, 03 May 2024 11:13:37 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 11:13:37 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 03 May 2024 11:13:37 GMT
ENV ARANGO_VERSION=3.12.0.2
# Fri, 03 May 2024 11:13:37 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 03 May 2024 11:13:37 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 03 May 2024 11:13:37 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 03 May 2024 11:13:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 May 2024 11:13:37 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 03 May 2024 11:13:37 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c6c464299418ea712993cb2f3c94ba89286c6e373921a08be6a506bf4e9b11`  
		Last Modified: Fri, 21 Jun 2024 01:57:28 GMT  
		Size: 301.1 MB (301126606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d363ca46bcc2fd49939bce38496b2623eb437a5da829687488a9aef0f12afe2`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4484419ad40939d2a8d59586c4c93713ac0f3280c28fcc522b370497d0e10e8d`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.0.2` - unknown; unknown

```console
$ docker pull arangodb@sha256:9b962121ad204153e5b4779d1eaa7351b688a51a9f6b46eb0c2640124f885dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 KB (440529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8edef511ac2d4b771c1de30e3cfd542ee56f0b9f6354a23e775c4f9adef7b17`

```dockerfile
```

-	Layers:
	-	`sha256:324d5c14295aef3b00263a4d8dcac0cea131640012528e5053cd58112f15c93d`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 426.1 KB (426072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f5a4286706b8b8e91d1a476201e00cd0437499fe79291b058585463add2d374`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 14.5 KB (14457 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:f1fa8f00c87ce7baea6f03085ed2a9cc4e3509dc098e8b2f164c3f2b4866554f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:37e593cdb44146fbe64b0e404407a174df22ee9b379262d7cfb5c1e8d9f1d3f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302162975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22810e5fe7473fcd9e24ea467d0dc5984aad8196b0e3623cbcc2a2ff2df6db4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Fri, 03 May 2024 11:13:37 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 11:13:37 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 03 May 2024 11:13:37 GMT
ENV ARANGO_VERSION=3.12.0.2
# Fri, 03 May 2024 11:13:37 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 03 May 2024 11:13:37 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 03 May 2024 11:13:37 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 03 May 2024 11:13:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 May 2024 11:13:37 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 03 May 2024 11:13:37 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e27b48c8fe935e54cfe60ef3e46dd5663da75405f18ec14ca26627c4c0ec87`  
		Last Modified: Thu, 20 Jun 2024 20:55:06 GMT  
		Size: 298.8 MB (298770856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da899acd957c7dde28a69cae008d106b7d9798c02abb60bb68e929e3c61b61d`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162d83bef531a5f2661a61373aec6ef7d443a12b2d9da806265c6d695851db9c`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:126383c986a5debc5b56aee1ccf6dc3fa57b7577ed67ba73690fda69dcb08261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.9 KB (334942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee995ef825f2cfe6a628ef9d08c7e986f980253d80e7f85a75fbfaf7bcca8d54`

```dockerfile
```

-	Layers:
	-	`sha256:a3b0687d6d0d3de2777bc0f49d8351560656047f1a5fee01b3ab2aec6f348947`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 320.8 KB (320773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd4fecd31e6f68f71a9f873f644baa34aa92db09933642d69c17ee6853ee295`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 14.2 KB (14169 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:2c16164a6bcc6cd3d9a2db7b22735d444d11b280643f7246798f46ee1a06b4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304401348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b421284ca5ae90a3b49e7d898574254a6bca120654a639535efafa7c098c7076`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Fri, 03 May 2024 11:13:37 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 11:13:37 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 03 May 2024 11:13:37 GMT
ENV ARANGO_VERSION=3.12.0.2
# Fri, 03 May 2024 11:13:37 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 03 May 2024 11:13:37 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 03 May 2024 11:13:37 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 03 May 2024 11:13:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 May 2024 11:13:37 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 03 May 2024 11:13:37 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c6c464299418ea712993cb2f3c94ba89286c6e373921a08be6a506bf4e9b11`  
		Last Modified: Fri, 21 Jun 2024 01:57:28 GMT  
		Size: 301.1 MB (301126606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d363ca46bcc2fd49939bce38496b2623eb437a5da829687488a9aef0f12afe2`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4484419ad40939d2a8d59586c4c93713ac0f3280c28fcc522b370497d0e10e8d`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:9b962121ad204153e5b4779d1eaa7351b688a51a9f6b46eb0c2640124f885dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 KB (440529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8edef511ac2d4b771c1de30e3cfd542ee56f0b9f6354a23e775c4f9adef7b17`

```dockerfile
```

-	Layers:
	-	`sha256:324d5c14295aef3b00263a4d8dcac0cea131640012528e5053cd58112f15c93d`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 426.1 KB (426072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f5a4286706b8b8e91d1a476201e00cd0437499fe79291b058585463add2d374`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 14.5 KB (14457 bytes)  
		MIME: application/vnd.in-toto+json
