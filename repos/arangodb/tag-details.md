<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.9`](#arangodb3119)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.0.2`](#arangodb31202)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:b9d98f8e8e09895824b6d30af039e0443587574bd075747f8155662f33ab80ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:7e2f9dc1790970ca34db8f04c2716f1b8d0d95048ce1ac836cdf73848ffc7380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.2 MB (252179402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749cb05754ac3e6f80ff97ce434a667b4da0dc572df51057be0b25c3dcbb2281`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
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
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3e0b5f1e2a1aae0881a60fa61ca291024e2a8fdda1bdb0e118eff43d6fc983`  
		Last Modified: Thu, 30 May 2024 20:56:48 GMT  
		Size: 248.8 MB (248797512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a71bd81b1f84402420b1bd0938c656063d6dc2560a64b39139070ed5f3b0924`  
		Last Modified: Thu, 30 May 2024 20:56:44 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9783538227bcce9a8b829ef1c3ffd4c6dec88af48ab582b64656e4acec67dba`  
		Last Modified: Thu, 30 May 2024 20:56:44 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3793000c3290f4469f95ed17dc2dba736d2c00ba9b2c36e3736b89e622939f58`  
		Last Modified: Thu, 30 May 2024 20:56:44 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:fc72303fe0ba72db0469ea60d110cd372ec76fe2c3e1e8d741229b365c8fee03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **907.5 KB (907534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a762f552fd2f9eb58d3f36b20cc11f9824bd1472bb933b586f0274275636475b`

```dockerfile
```

-	Layers:
	-	`sha256:963abda5ad769a4e585ce0b51977d7221680dede2a00b746525256e772a6c045`  
		Last Modified: Thu, 30 May 2024 20:56:44 GMT  
		Size: 892.0 KB (891997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:660174293bc2dc5f2aa3b1c6b8668d2d2be399d19cf19c5e2f53a623580c39a4`  
		Last Modified: Thu, 30 May 2024 20:56:44 GMT  
		Size: 15.5 KB (15537 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:228e81b3a9cc9133367eb301d2410b67394fa7a1718d89684f309e3bf8df8b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246128474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a161876b8afbe0d04382d3e4519b8d7dd602bcd613d0c0e9e929d2b0dbd97f26`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
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
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8016b2be0faf8ffeac8a34ce0da7c395c3d7019074a6b423a0011d7cca64107`  
		Last Modified: Thu, 30 May 2024 22:43:30 GMT  
		Size: 242.9 MB (242867704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9f4fcc9d07b2ed026aca6348bdc43f3c869b8aa22202f874f92eca49ef4d3f`  
		Last Modified: Thu, 30 May 2024 22:43:24 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b0739ed8718b876609d973079b049768e51a16343e80bf496dfed88cc36d5c`  
		Last Modified: Thu, 30 May 2024 22:43:25 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25ae8907826432efdfb99afe516fda992bc7b4224eda5d6d9dcd7d0bf2dca89`  
		Last Modified: Thu, 30 May 2024 22:43:25 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:6b4bb21306a7090b0b6e7565e6f4aa248eb0810b00cdd5dae4a813bd5c952454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1013097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfa3c8ea544528a609279d53312d6840a7594ec1f6a007f1e9e300e73fe7eef`

```dockerfile
```

-	Layers:
	-	`sha256:eea8d905980558e976feb14e582010acfd7f0f9b0affef5400470c0b5df14f53`  
		Last Modified: Thu, 30 May 2024 22:43:25 GMT  
		Size: 997.3 KB (997284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa261abbe78f2515cb55ce55935cf250cad3bfc583d06c99f4188f1494527e8c`  
		Last Modified: Thu, 30 May 2024 22:43:25 GMT  
		Size: 15.8 KB (15813 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.11.9`

```console
$ docker pull arangodb@sha256:b9d98f8e8e09895824b6d30af039e0443587574bd075747f8155662f33ab80ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11.9` - linux; amd64

```console
$ docker pull arangodb@sha256:7e2f9dc1790970ca34db8f04c2716f1b8d0d95048ce1ac836cdf73848ffc7380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.2 MB (252179402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749cb05754ac3e6f80ff97ce434a667b4da0dc572df51057be0b25c3dcbb2281`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
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
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3e0b5f1e2a1aae0881a60fa61ca291024e2a8fdda1bdb0e118eff43d6fc983`  
		Last Modified: Thu, 30 May 2024 20:56:48 GMT  
		Size: 248.8 MB (248797512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a71bd81b1f84402420b1bd0938c656063d6dc2560a64b39139070ed5f3b0924`  
		Last Modified: Thu, 30 May 2024 20:56:44 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9783538227bcce9a8b829ef1c3ffd4c6dec88af48ab582b64656e4acec67dba`  
		Last Modified: Thu, 30 May 2024 20:56:44 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3793000c3290f4469f95ed17dc2dba736d2c00ba9b2c36e3736b89e622939f58`  
		Last Modified: Thu, 30 May 2024 20:56:44 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.9` - unknown; unknown

```console
$ docker pull arangodb@sha256:fc72303fe0ba72db0469ea60d110cd372ec76fe2c3e1e8d741229b365c8fee03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **907.5 KB (907534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a762f552fd2f9eb58d3f36b20cc11f9824bd1472bb933b586f0274275636475b`

```dockerfile
```

-	Layers:
	-	`sha256:963abda5ad769a4e585ce0b51977d7221680dede2a00b746525256e772a6c045`  
		Last Modified: Thu, 30 May 2024 20:56:44 GMT  
		Size: 892.0 KB (891997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:660174293bc2dc5f2aa3b1c6b8668d2d2be399d19cf19c5e2f53a623580c39a4`  
		Last Modified: Thu, 30 May 2024 20:56:44 GMT  
		Size: 15.5 KB (15537 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11.9` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:228e81b3a9cc9133367eb301d2410b67394fa7a1718d89684f309e3bf8df8b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246128474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a161876b8afbe0d04382d3e4519b8d7dd602bcd613d0c0e9e929d2b0dbd97f26`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
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
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8016b2be0faf8ffeac8a34ce0da7c395c3d7019074a6b423a0011d7cca64107`  
		Last Modified: Thu, 30 May 2024 22:43:30 GMT  
		Size: 242.9 MB (242867704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9f4fcc9d07b2ed026aca6348bdc43f3c869b8aa22202f874f92eca49ef4d3f`  
		Last Modified: Thu, 30 May 2024 22:43:24 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b0739ed8718b876609d973079b049768e51a16343e80bf496dfed88cc36d5c`  
		Last Modified: Thu, 30 May 2024 22:43:25 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25ae8907826432efdfb99afe516fda992bc7b4224eda5d6d9dcd7d0bf2dca89`  
		Last Modified: Thu, 30 May 2024 22:43:25 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.9` - unknown; unknown

```console
$ docker pull arangodb@sha256:6b4bb21306a7090b0b6e7565e6f4aa248eb0810b00cdd5dae4a813bd5c952454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1013097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfa3c8ea544528a609279d53312d6840a7594ec1f6a007f1e9e300e73fe7eef`

```dockerfile
```

-	Layers:
	-	`sha256:eea8d905980558e976feb14e582010acfd7f0f9b0affef5400470c0b5df14f53`  
		Last Modified: Thu, 30 May 2024 22:43:25 GMT  
		Size: 997.3 KB (997284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa261abbe78f2515cb55ce55935cf250cad3bfc583d06c99f4188f1494527e8c`  
		Last Modified: Thu, 30 May 2024 22:43:25 GMT  
		Size: 15.8 KB (15813 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:68fc277b05f4a8cb71e213b5618c55fb7bb7b3b6fbe91837f75a78d264d8c503
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:6ba2e4284cd0f4835e3ef034be90fb947c3d61225d65d07e3b2d2d893e47de25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302152478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05880878202da31a773a239d353642c1ad6d112d8581b27adc3c5213a62fd2d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
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
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecb4552a8f3f176e5004c8da8ef025bc96f9970fec2ca1519a83f677501cfa6`  
		Last Modified: Thu, 30 May 2024 20:56:51 GMT  
		Size: 298.8 MB (298770918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a71bd81b1f84402420b1bd0938c656063d6dc2560a64b39139070ed5f3b0924`  
		Last Modified: Thu, 30 May 2024 20:56:44 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba35f16fa13d33de84fa2ae03283f5ed8562e2cfa79cd1e4fc83c794d2ae4f5`  
		Last Modified: Thu, 30 May 2024 20:56:45 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:3ae457d72e4333b3c551472c7299cd0b7549909708644a7717c2b65b20b948f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.9 KB (334892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5eb8581c382ce3d8f167e805aea55ec4f031b76b22efe534034ce0fcd746611`

```dockerfile
```

-	Layers:
	-	`sha256:a9d33191e48a82cc386bf8fb085e98d39155ab410ec83f0b34f72f97f803ee78`  
		Last Modified: Thu, 30 May 2024 20:56:45 GMT  
		Size: 320.8 KB (320771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d43371927f12c125f842fdb363341382fc8d9ae8877611a4ed80e3edf38670b`  
		Last Modified: Thu, 30 May 2024 20:56:46 GMT  
		Size: 14.1 KB (14121 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:77a0a6a6e1610ab75e74ada4dad3136810cd5643191d58ddd32279abf5138141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304386985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a31466dd07eaaa38f6f93f0432cf83534ea71459e53636f1a5dc96e8dbf923`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
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
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e33c47e876b44f73880d564f7d967d19f227534bff6b123cce3c086be64343`  
		Last Modified: Thu, 30 May 2024 22:44:39 GMT  
		Size: 301.1 MB (301126546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331b04b69765d6876f3d93d21b7eeea124c3b323fd30ece36f2977a0a52a3e38`  
		Last Modified: Thu, 30 May 2024 22:44:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b3bbe9fb54c96d348bb5a892bea50fed5fb01a6321b5bc7577d344f3c4f3ac`  
		Last Modified: Thu, 30 May 2024 22:44:33 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:7e3c32cbc3cdfffdf705ec3f05b4caafbec987c470902e501c649b094e66e7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 KB (440479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a311b2b1a8154ec6677fb0acf8f74a3996c79f0e291e32b8766f92423fe3dd70`

```dockerfile
```

-	Layers:
	-	`sha256:d8309cda65dfffe48e090a0e8f3887d57544aecc6294e2cf591e58bb1b188021`  
		Last Modified: Thu, 30 May 2024 22:44:34 GMT  
		Size: 426.1 KB (426070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d42abdd45b6394a0e82d223a8efb8e983059a01c752246b637db026c180d560a`  
		Last Modified: Thu, 30 May 2024 22:44:33 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.0.2`

```console
$ docker pull arangodb@sha256:68fc277b05f4a8cb71e213b5618c55fb7bb7b3b6fbe91837f75a78d264d8c503
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12.0.2` - linux; amd64

```console
$ docker pull arangodb@sha256:6ba2e4284cd0f4835e3ef034be90fb947c3d61225d65d07e3b2d2d893e47de25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302152478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05880878202da31a773a239d353642c1ad6d112d8581b27adc3c5213a62fd2d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
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
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecb4552a8f3f176e5004c8da8ef025bc96f9970fec2ca1519a83f677501cfa6`  
		Last Modified: Thu, 30 May 2024 20:56:51 GMT  
		Size: 298.8 MB (298770918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a71bd81b1f84402420b1bd0938c656063d6dc2560a64b39139070ed5f3b0924`  
		Last Modified: Thu, 30 May 2024 20:56:44 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba35f16fa13d33de84fa2ae03283f5ed8562e2cfa79cd1e4fc83c794d2ae4f5`  
		Last Modified: Thu, 30 May 2024 20:56:45 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.0.2` - unknown; unknown

```console
$ docker pull arangodb@sha256:3ae457d72e4333b3c551472c7299cd0b7549909708644a7717c2b65b20b948f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.9 KB (334892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5eb8581c382ce3d8f167e805aea55ec4f031b76b22efe534034ce0fcd746611`

```dockerfile
```

-	Layers:
	-	`sha256:a9d33191e48a82cc386bf8fb085e98d39155ab410ec83f0b34f72f97f803ee78`  
		Last Modified: Thu, 30 May 2024 20:56:45 GMT  
		Size: 320.8 KB (320771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d43371927f12c125f842fdb363341382fc8d9ae8877611a4ed80e3edf38670b`  
		Last Modified: Thu, 30 May 2024 20:56:46 GMT  
		Size: 14.1 KB (14121 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12.0.2` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:77a0a6a6e1610ab75e74ada4dad3136810cd5643191d58ddd32279abf5138141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304386985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a31466dd07eaaa38f6f93f0432cf83534ea71459e53636f1a5dc96e8dbf923`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
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
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e33c47e876b44f73880d564f7d967d19f227534bff6b123cce3c086be64343`  
		Last Modified: Thu, 30 May 2024 22:44:39 GMT  
		Size: 301.1 MB (301126546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331b04b69765d6876f3d93d21b7eeea124c3b323fd30ece36f2977a0a52a3e38`  
		Last Modified: Thu, 30 May 2024 22:44:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b3bbe9fb54c96d348bb5a892bea50fed5fb01a6321b5bc7577d344f3c4f3ac`  
		Last Modified: Thu, 30 May 2024 22:44:33 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.0.2` - unknown; unknown

```console
$ docker pull arangodb@sha256:7e3c32cbc3cdfffdf705ec3f05b4caafbec987c470902e501c649b094e66e7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 KB (440479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a311b2b1a8154ec6677fb0acf8f74a3996c79f0e291e32b8766f92423fe3dd70`

```dockerfile
```

-	Layers:
	-	`sha256:d8309cda65dfffe48e090a0e8f3887d57544aecc6294e2cf591e58bb1b188021`  
		Last Modified: Thu, 30 May 2024 22:44:34 GMT  
		Size: 426.1 KB (426070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d42abdd45b6394a0e82d223a8efb8e983059a01c752246b637db026c180d560a`  
		Last Modified: Thu, 30 May 2024 22:44:33 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:68fc277b05f4a8cb71e213b5618c55fb7bb7b3b6fbe91837f75a78d264d8c503
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:6ba2e4284cd0f4835e3ef034be90fb947c3d61225d65d07e3b2d2d893e47de25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302152478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05880878202da31a773a239d353642c1ad6d112d8581b27adc3c5213a62fd2d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
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
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecb4552a8f3f176e5004c8da8ef025bc96f9970fec2ca1519a83f677501cfa6`  
		Last Modified: Thu, 30 May 2024 20:56:51 GMT  
		Size: 298.8 MB (298770918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a71bd81b1f84402420b1bd0938c656063d6dc2560a64b39139070ed5f3b0924`  
		Last Modified: Thu, 30 May 2024 20:56:44 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba35f16fa13d33de84fa2ae03283f5ed8562e2cfa79cd1e4fc83c794d2ae4f5`  
		Last Modified: Thu, 30 May 2024 20:56:45 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:3ae457d72e4333b3c551472c7299cd0b7549909708644a7717c2b65b20b948f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.9 KB (334892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5eb8581c382ce3d8f167e805aea55ec4f031b76b22efe534034ce0fcd746611`

```dockerfile
```

-	Layers:
	-	`sha256:a9d33191e48a82cc386bf8fb085e98d39155ab410ec83f0b34f72f97f803ee78`  
		Last Modified: Thu, 30 May 2024 20:56:45 GMT  
		Size: 320.8 KB (320771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d43371927f12c125f842fdb363341382fc8d9ae8877611a4ed80e3edf38670b`  
		Last Modified: Thu, 30 May 2024 20:56:46 GMT  
		Size: 14.1 KB (14121 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:77a0a6a6e1610ab75e74ada4dad3136810cd5643191d58ddd32279abf5138141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304386985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a31466dd07eaaa38f6f93f0432cf83534ea71459e53636f1a5dc96e8dbf923`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
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
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e33c47e876b44f73880d564f7d967d19f227534bff6b123cce3c086be64343`  
		Last Modified: Thu, 30 May 2024 22:44:39 GMT  
		Size: 301.1 MB (301126546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331b04b69765d6876f3d93d21b7eeea124c3b323fd30ece36f2977a0a52a3e38`  
		Last Modified: Thu, 30 May 2024 22:44:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b3bbe9fb54c96d348bb5a892bea50fed5fb01a6321b5bc7577d344f3c4f3ac`  
		Last Modified: Thu, 30 May 2024 22:44:33 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:7e3c32cbc3cdfffdf705ec3f05b4caafbec987c470902e501c649b094e66e7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 KB (440479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a311b2b1a8154ec6677fb0acf8f74a3996c79f0e291e32b8766f92423fe3dd70`

```dockerfile
```

-	Layers:
	-	`sha256:d8309cda65dfffe48e090a0e8f3887d57544aecc6294e2cf591e58bb1b188021`  
		Last Modified: Thu, 30 May 2024 22:44:34 GMT  
		Size: 426.1 KB (426070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d42abdd45b6394a0e82d223a8efb8e983059a01c752246b637db026c180d560a`  
		Last Modified: Thu, 30 May 2024 22:44:33 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
