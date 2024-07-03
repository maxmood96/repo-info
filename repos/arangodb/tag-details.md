<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.10`](#arangodb31110)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.0.2`](#arangodb31202)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:7baa19d766b7cc62375f6899bb113f63c954bd756fd0cd3a76828898ffca992a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:81106da6160a126fbc9b51e9b6532950da2172736a1b5c583594f0664a56125e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.2 MB (252189234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ecf981a2b3b2842459c4029e11c470d0a74362f01867960132b6ee3df311321`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sun, 26 May 2024 22:11:33 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Sun, 26 May 2024 22:11:33 GMT
CMD ["/bin/sh"]
# Sun, 26 May 2024 22:11:33 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sun, 26 May 2024 22:11:33 GMT
ENV ARANGO_VERSION=3.11.9
# Sun, 26 May 2024 22:11:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Sun, 26 May 2024 22:11:33 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sun, 26 May 2024 22:11:33 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Sun, 26 May 2024 22:11:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sun, 26 May 2024 22:11:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sun, 26 May 2024 22:11:33 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Sun, 26 May 2024 22:11:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 26 May 2024 22:11:33 GMT
EXPOSE map[8529/tcp:{}]
# Sun, 26 May 2024 22:11:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b77acb53f30b0ef34ff0061fb32e83c9d64f2fc6eb6264c7b1d3d3679cf5f8b`  
		Last Modified: Thu, 20 Jun 2024 20:55:05 GMT  
		Size: 248.8 MB (248796782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536886790630047471852b4c20a275cfd471a3de9cce4ed0e4aed73f006efee6`  
		Last Modified: Thu, 20 Jun 2024 20:55:02 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a30e6508a84d300a730e7b40eaede5ef7c2963d42702ee261af99fb053f0d4`  
		Last Modified: Thu, 20 Jun 2024 20:55:02 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfda4b6bfd3f68738c5c9028f9629d02d1f7da5ffbf5b1b3c6454757057b8b3`  
		Last Modified: Thu, 20 Jun 2024 20:55:02 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:7a2ba89afc76958ee1ed35b13218dfa085444179e5b743aa533b673989404223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **907.6 KB (907555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb03bec5b3c8da6dce2e7687a689a4585773fb7ea034f9c8b6dda50ff9b444df`

```dockerfile
```

-	Layers:
	-	`sha256:beb4f1a1941806f18f99647e9fefce2f68d1193e58ae88d9a3d393865e13ec70`  
		Last Modified: Thu, 20 Jun 2024 20:55:02 GMT  
		Size: 892.0 KB (891969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb69aa424c82d6ad4f1e02849d421572746012ae5addafb6f1adfb378fd590b`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 15.6 KB (15586 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:50597da391bc31f367bc07e9feffc8e290c7c8d33f5cd0f2a69b739d913ab1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246145638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5ca34356a8d952b3f05f9044766b5e8df2e8af456acb7c7b38d7d2782d19b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sun, 26 May 2024 22:11:33 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Sun, 26 May 2024 22:11:33 GMT
CMD ["/bin/sh"]
# Sun, 26 May 2024 22:11:33 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sun, 26 May 2024 22:11:33 GMT
ENV ARANGO_VERSION=3.11.9
# Sun, 26 May 2024 22:11:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Sun, 26 May 2024 22:11:33 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sun, 26 May 2024 22:11:33 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Sun, 26 May 2024 22:11:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sun, 26 May 2024 22:11:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sun, 26 May 2024 22:11:33 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Sun, 26 May 2024 22:11:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 26 May 2024 22:11:33 GMT
EXPOSE map[8529/tcp:{}]
# Sun, 26 May 2024 22:11:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b1059f69acb6269bca7b97eaa776c1d7f9360c87e7bee064e82b45010f20a3`  
		Last Modified: Thu, 20 Jun 2024 22:36:58 GMT  
		Size: 242.9 MB (242870564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1293fce9d9f9c40a0306aa9f0e6fdd28ac773b67a9e94058099748f64bb64519`  
		Last Modified: Thu, 20 Jun 2024 22:36:51 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18081c175c1beb342c3af1705e9d6ac67bb01ab6c881f12d1754002f71447843`  
		Last Modified: Thu, 20 Jun 2024 22:36:51 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd5640881219ac57b0bc2357a97ff2b0c5accd3836fcf431122d7eaddb8612d`  
		Last Modified: Thu, 20 Jun 2024 22:36:53 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:c4343562509cebdac7c26741864dc6e1cb0e635789aa22e9f59cf4e7489fa54e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1013118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba91cf256e15561acab3946b5545eba5d91c6a1bf13de018f70793610703236`

```dockerfile
```

-	Layers:
	-	`sha256:142235d72167ebc07cc2765f4aca2b2631d27b3d5e53e86044d1afc040ce3fdd`  
		Last Modified: Thu, 20 Jun 2024 22:36:52 GMT  
		Size: 997.3 KB (997256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9305498b65be3489c44621f46d46da1defe79b0deacd45d4fc917f93a55de147`  
		Last Modified: Thu, 20 Jun 2024 22:36:51 GMT  
		Size: 15.9 KB (15862 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.11.10`

```console
$ docker pull arangodb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

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
