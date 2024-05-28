<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.9`](#arangodb3119)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.0.2`](#arangodb31202)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:e56f745b2948d3b324709ee72dbd344a86987af1dcc6d28d41c4f5d9d0cfe7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:1404e102feb3e9378b0fc42422f7b246a7fce2eb74f340c5046a5cf16f46bdec
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.2 MB (252162802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccc6a318635e209138bd9463f9ed37c7369e415f6dae1f8f7459f6e400bf989`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 28 May 2024 19:37:05 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 28 May 2024 19:37:05 GMT
ENV ARANGO_VERSION=3.11.9
# Tue, 28 May 2024 19:37:37 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 28 May 2024 19:37:38 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 28 May 2024 19:37:39 GMT
RUN echo "UTC" > /etc/timezone
# Tue, 28 May 2024 19:37:39 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 28 May 2024 19:37:39 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 28 May 2024 19:37:39 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 28 May 2024 19:37:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 May 2024 19:37:40 GMT
EXPOSE 8529
# Tue, 28 May 2024 19:37:40 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a19f0612bf8931fbc9dd584302bae041690177dac96bbeffacdeafbb86617fc`  
		Last Modified: Tue, 28 May 2024 19:38:19 GMT  
		Size: 248.8 MB (248780910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac76ec7eaae83200c646ac62dff47fd118601d4fbbf275476f3cc1704ab6877b`  
		Last Modified: Tue, 28 May 2024 19:37:55 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5b27795d976a515c5aa4ff4da5017652cb9897ba4c8b0a12fb2672a4e754fa`  
		Last Modified: Tue, 28 May 2024 19:37:55 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fea8b6956914b3910a1f88c8dd88a81c38ae95b9e4381016619405a43c0de71`  
		Last Modified: Tue, 28 May 2024 19:37:55 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:d20e7b4e72fb0a5579735ae68276964d7511d2152f2a27d8a24e238450fa640d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246112402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b59a6f1f3083c25095d624c18f090437c91f158fdc6316ecd2d6de2b7a18dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Tue, 28 May 2024 19:40:56 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 28 May 2024 19:40:56 GMT
ENV ARANGO_VERSION=3.11.9
# Tue, 28 May 2024 19:41:27 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 28 May 2024 19:41:32 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 28 May 2024 19:41:32 GMT
RUN echo "UTC" > /etc/timezone
# Tue, 28 May 2024 19:41:32 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 28 May 2024 19:41:32 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 28 May 2024 19:41:32 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 28 May 2024 19:41:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 May 2024 19:41:32 GMT
EXPOSE 8529
# Tue, 28 May 2024 19:41:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b6dfd18dc72f8a34d46552b4bf003ce805a79df8a8fd176422fca31d8649fd`  
		Last Modified: Tue, 28 May 2024 19:42:02 GMT  
		Size: 242.9 MB (242851633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e51e3ced9919157de34c5ed6e0b083cd44fc6d0c51a60f8da8336f86474f72`  
		Last Modified: Tue, 28 May 2024 19:41:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f29de4f7314d21e08d9d3931341362ab92991b5d48418b7ae2229f1ddc25889`  
		Last Modified: Tue, 28 May 2024 19:41:45 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489e1bca3a0c1ad7fe207c0f2d5e8307d8b3135f4572f9636654c332e24f3043`  
		Last Modified: Tue, 28 May 2024 19:41:45 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.11.9`

```console
$ docker pull arangodb@sha256:e56f745b2948d3b324709ee72dbd344a86987af1dcc6d28d41c4f5d9d0cfe7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.11.9` - linux; amd64

```console
$ docker pull arangodb@sha256:1404e102feb3e9378b0fc42422f7b246a7fce2eb74f340c5046a5cf16f46bdec
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.2 MB (252162802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccc6a318635e209138bd9463f9ed37c7369e415f6dae1f8f7459f6e400bf989`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 28 May 2024 19:37:05 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 28 May 2024 19:37:05 GMT
ENV ARANGO_VERSION=3.11.9
# Tue, 28 May 2024 19:37:37 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 28 May 2024 19:37:38 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 28 May 2024 19:37:39 GMT
RUN echo "UTC" > /etc/timezone
# Tue, 28 May 2024 19:37:39 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 28 May 2024 19:37:39 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 28 May 2024 19:37:39 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 28 May 2024 19:37:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 May 2024 19:37:40 GMT
EXPOSE 8529
# Tue, 28 May 2024 19:37:40 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a19f0612bf8931fbc9dd584302bae041690177dac96bbeffacdeafbb86617fc`  
		Last Modified: Tue, 28 May 2024 19:38:19 GMT  
		Size: 248.8 MB (248780910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac76ec7eaae83200c646ac62dff47fd118601d4fbbf275476f3cc1704ab6877b`  
		Last Modified: Tue, 28 May 2024 19:37:55 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5b27795d976a515c5aa4ff4da5017652cb9897ba4c8b0a12fb2672a4e754fa`  
		Last Modified: Tue, 28 May 2024 19:37:55 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fea8b6956914b3910a1f88c8dd88a81c38ae95b9e4381016619405a43c0de71`  
		Last Modified: Tue, 28 May 2024 19:37:55 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.11.9` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:d20e7b4e72fb0a5579735ae68276964d7511d2152f2a27d8a24e238450fa640d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246112402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b59a6f1f3083c25095d624c18f090437c91f158fdc6316ecd2d6de2b7a18dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Tue, 28 May 2024 19:40:56 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 28 May 2024 19:40:56 GMT
ENV ARANGO_VERSION=3.11.9
# Tue, 28 May 2024 19:41:27 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 28 May 2024 19:41:32 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 28 May 2024 19:41:32 GMT
RUN echo "UTC" > /etc/timezone
# Tue, 28 May 2024 19:41:32 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 28 May 2024 19:41:32 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 28 May 2024 19:41:32 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 28 May 2024 19:41:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 May 2024 19:41:32 GMT
EXPOSE 8529
# Tue, 28 May 2024 19:41:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b6dfd18dc72f8a34d46552b4bf003ce805a79df8a8fd176422fca31d8649fd`  
		Last Modified: Tue, 28 May 2024 19:42:02 GMT  
		Size: 242.9 MB (242851633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e51e3ced9919157de34c5ed6e0b083cd44fc6d0c51a60f8da8336f86474f72`  
		Last Modified: Tue, 28 May 2024 19:41:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f29de4f7314d21e08d9d3931341362ab92991b5d48418b7ae2229f1ddc25889`  
		Last Modified: Tue, 28 May 2024 19:41:45 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489e1bca3a0c1ad7fe207c0f2d5e8307d8b3135f4572f9636654c332e24f3043`  
		Last Modified: Tue, 28 May 2024 19:41:45 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:dd6a9b04252c0af8a18b810391e4281be386cc71d5017e8f5c83d34c664f97be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:ece1e3f00233924b41233c8a9de04582f09915afd230caeda23829556dd19750
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302150631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68383e088cf03d9df46df0bd99d32a500ffeab1c6646477c210b26cfb5ba4870`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Mon, 25 Mar 2024 19:51:03 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 06 May 2024 18:35:50 GMT
ENV ARANGO_VERSION=3.12.0.2
# Mon, 06 May 2024 18:36:17 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 06 May 2024 18:36:19 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 06 May 2024 18:36:20 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 06 May 2024 18:36:20 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 06 May 2024 18:36:20 GMT
COPY file:513375723ea161120e77fe867a15962ee909f21d5ad9010e94f567e75f817d04 in /entrypoint.sh 
# Mon, 06 May 2024 18:36:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 May 2024 18:36:20 GMT
EXPOSE 8529
# Mon, 06 May 2024 18:36:20 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee05a51391ef930a2f5dd135e679f29ba04eddb246d55b8e3464092748d00e18`  
		Last Modified: Mon, 06 May 2024 18:36:59 GMT  
		Size: 298.8 MB (298769074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd74f121790fe3ae825c1755bc052006799800c460b0fb7bedc3e743f933079a`  
		Last Modified: Mon, 06 May 2024 18:36:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2afb99c8efe11f1b6e1765a6668849791c614d7604b4d2ff6060229cb20685`  
		Last Modified: Mon, 06 May 2024 18:36:31 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:0c0c613dc3a10592e8643403e44fe7a92a20976cda38403bad88c75e6ca0d76e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304386726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19e648f21425026668926f4262f551656aba3782bb0d9d6866f4911076b2d96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Mon, 25 Mar 2024 20:07:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 06 May 2024 19:34:22 GMT
ENV ARANGO_VERSION=3.12.0.2
# Mon, 06 May 2024 19:34:45 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 06 May 2024 19:34:50 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 06 May 2024 19:34:50 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 06 May 2024 19:34:50 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 06 May 2024 19:34:50 GMT
COPY file:513375723ea161120e77fe867a15962ee909f21d5ad9010e94f567e75f817d04 in /entrypoint.sh 
# Mon, 06 May 2024 19:34:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 May 2024 19:34:50 GMT
EXPOSE 8529
# Mon, 06 May 2024 19:34:51 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9f7bac526f3b2c34cac23ce8300d3f8b4069e940003168344ef221d9e456cc`  
		Last Modified: Mon, 06 May 2024 19:35:25 GMT  
		Size: 301.1 MB (301126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9f07f0110e7433d953818d5d26b4fcd5f6024694eb2c53bfb67413c771e0b9`  
		Last Modified: Mon, 06 May 2024 19:35:03 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826d90065a60b541021d4abbfdec078fda277c1db4995051b63e43d03d6ad3cf`  
		Last Modified: Mon, 06 May 2024 19:35:03 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.12.0.2`

```console
$ docker pull arangodb@sha256:dd6a9b04252c0af8a18b810391e4281be386cc71d5017e8f5c83d34c664f97be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.12.0.2` - linux; amd64

```console
$ docker pull arangodb@sha256:ece1e3f00233924b41233c8a9de04582f09915afd230caeda23829556dd19750
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302150631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68383e088cf03d9df46df0bd99d32a500ffeab1c6646477c210b26cfb5ba4870`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Mon, 25 Mar 2024 19:51:03 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 06 May 2024 18:35:50 GMT
ENV ARANGO_VERSION=3.12.0.2
# Mon, 06 May 2024 18:36:17 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 06 May 2024 18:36:19 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 06 May 2024 18:36:20 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 06 May 2024 18:36:20 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 06 May 2024 18:36:20 GMT
COPY file:513375723ea161120e77fe867a15962ee909f21d5ad9010e94f567e75f817d04 in /entrypoint.sh 
# Mon, 06 May 2024 18:36:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 May 2024 18:36:20 GMT
EXPOSE 8529
# Mon, 06 May 2024 18:36:20 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee05a51391ef930a2f5dd135e679f29ba04eddb246d55b8e3464092748d00e18`  
		Last Modified: Mon, 06 May 2024 18:36:59 GMT  
		Size: 298.8 MB (298769074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd74f121790fe3ae825c1755bc052006799800c460b0fb7bedc3e743f933079a`  
		Last Modified: Mon, 06 May 2024 18:36:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2afb99c8efe11f1b6e1765a6668849791c614d7604b4d2ff6060229cb20685`  
		Last Modified: Mon, 06 May 2024 18:36:31 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.12.0.2` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:0c0c613dc3a10592e8643403e44fe7a92a20976cda38403bad88c75e6ca0d76e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304386726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19e648f21425026668926f4262f551656aba3782bb0d9d6866f4911076b2d96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Mon, 25 Mar 2024 20:07:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 06 May 2024 19:34:22 GMT
ENV ARANGO_VERSION=3.12.0.2
# Mon, 06 May 2024 19:34:45 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 06 May 2024 19:34:50 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 06 May 2024 19:34:50 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 06 May 2024 19:34:50 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 06 May 2024 19:34:50 GMT
COPY file:513375723ea161120e77fe867a15962ee909f21d5ad9010e94f567e75f817d04 in /entrypoint.sh 
# Mon, 06 May 2024 19:34:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 May 2024 19:34:50 GMT
EXPOSE 8529
# Mon, 06 May 2024 19:34:51 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9f7bac526f3b2c34cac23ce8300d3f8b4069e940003168344ef221d9e456cc`  
		Last Modified: Mon, 06 May 2024 19:35:25 GMT  
		Size: 301.1 MB (301126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9f07f0110e7433d953818d5d26b4fcd5f6024694eb2c53bfb67413c771e0b9`  
		Last Modified: Mon, 06 May 2024 19:35:03 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826d90065a60b541021d4abbfdec078fda277c1db4995051b63e43d03d6ad3cf`  
		Last Modified: Mon, 06 May 2024 19:35:03 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:dd6a9b04252c0af8a18b810391e4281be386cc71d5017e8f5c83d34c664f97be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:ece1e3f00233924b41233c8a9de04582f09915afd230caeda23829556dd19750
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302150631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68383e088cf03d9df46df0bd99d32a500ffeab1c6646477c210b26cfb5ba4870`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Mon, 25 Mar 2024 19:51:03 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 06 May 2024 18:35:50 GMT
ENV ARANGO_VERSION=3.12.0.2
# Mon, 06 May 2024 18:36:17 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 06 May 2024 18:36:19 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 06 May 2024 18:36:20 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 06 May 2024 18:36:20 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 06 May 2024 18:36:20 GMT
COPY file:513375723ea161120e77fe867a15962ee909f21d5ad9010e94f567e75f817d04 in /entrypoint.sh 
# Mon, 06 May 2024 18:36:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 May 2024 18:36:20 GMT
EXPOSE 8529
# Mon, 06 May 2024 18:36:20 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee05a51391ef930a2f5dd135e679f29ba04eddb246d55b8e3464092748d00e18`  
		Last Modified: Mon, 06 May 2024 18:36:59 GMT  
		Size: 298.8 MB (298769074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd74f121790fe3ae825c1755bc052006799800c460b0fb7bedc3e743f933079a`  
		Last Modified: Mon, 06 May 2024 18:36:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2afb99c8efe11f1b6e1765a6668849791c614d7604b4d2ff6060229cb20685`  
		Last Modified: Mon, 06 May 2024 18:36:31 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:0c0c613dc3a10592e8643403e44fe7a92a20976cda38403bad88c75e6ca0d76e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304386726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19e648f21425026668926f4262f551656aba3782bb0d9d6866f4911076b2d96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Mon, 25 Mar 2024 20:07:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 06 May 2024 19:34:22 GMT
ENV ARANGO_VERSION=3.12.0.2
# Mon, 06 May 2024 19:34:45 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 06 May 2024 19:34:50 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 06 May 2024 19:34:50 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 06 May 2024 19:34:50 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 06 May 2024 19:34:50 GMT
COPY file:513375723ea161120e77fe867a15962ee909f21d5ad9010e94f567e75f817d04 in /entrypoint.sh 
# Mon, 06 May 2024 19:34:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 May 2024 19:34:50 GMT
EXPOSE 8529
# Mon, 06 May 2024 19:34:51 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9f7bac526f3b2c34cac23ce8300d3f8b4069e940003168344ef221d9e456cc`  
		Last Modified: Mon, 06 May 2024 19:35:25 GMT  
		Size: 301.1 MB (301126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9f07f0110e7433d953818d5d26b4fcd5f6024694eb2c53bfb67413c771e0b9`  
		Last Modified: Mon, 06 May 2024 19:35:03 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826d90065a60b541021d4abbfdec078fda277c1db4995051b63e43d03d6ad3cf`  
		Last Modified: Mon, 06 May 2024 19:35:03 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
