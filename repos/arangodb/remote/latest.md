## `arangodb:latest`

```console
$ docker pull arangodb@sha256:1e75d74954a49f5c5d45913e81ad278585c7ffd9331bfbfd53c6e9a909d84a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:16893e767f47d28e3297839637741e5c4023e815adf860dfc674e1a36c7c7db0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.4 MB (249404256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2753be2cd85b4b119d5893fe40763b5db14fd62d65e7948ac3e982b415cbe22f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:18:53 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 16 Mar 2024 06:19:28 GMT
ENV ARANGO_VERSION=3.11.8
# Sat, 16 Mar 2024 06:19:55 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 16 Mar 2024 06:19:57 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 16 Mar 2024 06:19:58 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 16 Mar 2024 06:19:58 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 16 Mar 2024 06:19:58 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 16 Mar 2024 06:19:58 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 16 Mar 2024 06:19:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 06:19:58 GMT
EXPOSE 8529
# Sat, 16 Mar 2024 06:19:58 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f3f691dd025a65a1f705ffb6d571287717664383a6b9fea0fee6b74430d2a8`  
		Last Modified: Sat, 16 Mar 2024 06:21:00 GMT  
		Size: 246.6 MB (246593932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be28253d1a0915171fc6f15ba590882a22b37bdef086d7931dd7586c2f1761b`  
		Last Modified: Sat, 16 Mar 2024 06:20:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80520ffcf501e8d24f340177e83997d625f414247df98144f076dc22b316c6e4`  
		Last Modified: Sat, 16 Mar 2024 06:20:38 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89e0cc1f692c2e4f754606d4a486e127f29d7eb7aa7540a9fdac0c878a257fa`  
		Last Modified: Sat, 16 Mar 2024 06:20:38 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:3f8be0114b280db211838c5c1eeb7bb3c271d1b8acbcd93e8ffe757ec8b0113d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243547838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3dec3550f513a45281a571ecea1b3621ceb2a07e997e471d93c4b1abbbd7e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:53:30 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 16 Mar 2024 02:54:03 GMT
ENV ARANGO_VERSION=3.11.8
# Sat, 16 Mar 2024 02:54:28 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 16 Mar 2024 02:54:32 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 16 Mar 2024 02:54:33 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 16 Mar 2024 02:54:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 16 Mar 2024 02:54:33 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 16 Mar 2024 02:54:33 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 16 Mar 2024 02:54:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:54:33 GMT
EXPOSE 8529
# Sat, 16 Mar 2024 02:54:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ed7edc540d36b1d3c35c5f194f5198953fb9ac4f63649afdb98f68c0b3ba81`  
		Last Modified: Sat, 16 Mar 2024 02:55:25 GMT  
		Size: 240.8 MB (240837069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b2d8588faf04eed3cd34d9a936697948a3f834b3a17cded688b5907562c5ec`  
		Last Modified: Sat, 16 Mar 2024 02:55:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030474d2d49837281cdd335832ce82999f881dd31f3b71d14d49915b3ea19341`  
		Last Modified: Sat, 16 Mar 2024 02:55:08 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a7ff06092e552d9d88c89c167e27b859037542d556a711e62ae1e34c3852e1`  
		Last Modified: Sat, 16 Mar 2024 02:55:08 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
