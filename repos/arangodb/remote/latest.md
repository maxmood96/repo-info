## `arangodb:latest`

```console
$ docker pull arangodb@sha256:a831f2663e587e264c1ba5d0656ed510832c3b3d2255dcbb2877d5fc00be9539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:25b9c382d39258cdec3765c346a0527a29c8a7efa377c62facf7895a8ffee42d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250499308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3879e5a9e57a3d991dc1ed882ac60b63c782ca4b9c43d3d27ef78f8b1cfc31a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:33:45 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 27 Feb 2024 01:29:26 GMT
ENV ARANGO_VERSION=3.11.8
# Tue, 27 Feb 2024 01:29:52 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 27 Feb 2024 01:29:54 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 27 Feb 2024 01:29:55 GMT
RUN echo "UTC" > /etc/timezone
# Tue, 27 Feb 2024 01:29:55 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 27 Feb 2024 01:29:55 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 27 Feb 2024 01:29:55 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 27 Feb 2024 01:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 Feb 2024 01:29:55 GMT
EXPOSE 8529
# Tue, 27 Feb 2024 01:29:55 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c05c32988fac2ebee2bf76c78b2a2588296e786f77ab58e0b6f0a4cfee621d`  
		Last Modified: Tue, 27 Feb 2024 01:30:34 GMT  
		Size: 247.7 MB (247688983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d955a907b5eb4e59e3c500729ae3da06da1207ed8ac10dbf4631e1b9f207a97`  
		Last Modified: Tue, 27 Feb 2024 01:30:11 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7498016b576625ac44fa06868b1d9b3c8ce8894c118bb3a58c0ea8138107fa`  
		Last Modified: Tue, 27 Feb 2024 01:30:11 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9861bf6ac609fa8fc21efdc54a0aa369f73f3f64f52ae09604de057fe87964a6`  
		Last Modified: Tue, 27 Feb 2024 01:30:11 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:886889141b11f219711df6b4335f4cfc8864d364d1a7cfa07274a3cae0d928e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244638704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d57d7108f711180b3e83b4ecbfdb105bbc5e2601816cd1da3aa72cf351eb14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:39:03 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 27 Feb 2024 00:26:36 GMT
ENV ARANGO_VERSION=3.11.8
# Tue, 27 Feb 2024 00:27:03 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 27 Feb 2024 00:27:07 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 27 Feb 2024 00:27:08 GMT
RUN echo "UTC" > /etc/timezone
# Tue, 27 Feb 2024 00:27:08 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 27 Feb 2024 00:27:08 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 27 Feb 2024 00:27:08 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 27 Feb 2024 00:27:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 Feb 2024 00:27:08 GMT
EXPOSE 8529
# Tue, 27 Feb 2024 00:27:08 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5a7242f8e774cd92ac52b857efaf869598adeb420486ad9a324792ae117791`  
		Last Modified: Tue, 27 Feb 2024 00:27:40 GMT  
		Size: 241.9 MB (241927935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be19f420545323ca5bb84dabd119308035fc37c284db32b1ba55234b544dd3`  
		Last Modified: Tue, 27 Feb 2024 00:27:23 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af17a3941e26344618420037b396bfee4ab7d41280be0498ad0531b6c02f2be`  
		Last Modified: Tue, 27 Feb 2024 00:27:23 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c230a5ec14b6a73e848a400d8ee1f8c1baf29cd080c6398c79e980488bc5aa0c`  
		Last Modified: Tue, 27 Feb 2024 00:27:23 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
