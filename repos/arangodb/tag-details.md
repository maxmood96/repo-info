<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.10`](#arangodb310)
-	[`arangodb:3.10.13`](#arangodb31013)
-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.8`](#arangodb3118)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.10`

```console
$ docker pull arangodb@sha256:2fc2d3996cbb945647b793dd8e79950445fa7b90c9a99dbca59c8603114e82ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10` - linux; amd64

```console
$ docker pull arangodb@sha256:b671d8f118c7a6a9a1596f5f76fe80dd32d99e1b164f9e4cd042dd178adde57f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225641490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9dcd7adf87108998b35fd7b78799113a4c7fd138ae366d602534ba20f73780`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:33:45 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 31 Jan 2024 20:35:25 GMT
ENV ARANGO_VERSION=3.10.13
# Wed, 31 Jan 2024 20:35:53 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 31 Jan 2024 20:35:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 31 Jan 2024 20:35:55 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 31 Jan 2024 20:35:55 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 31 Jan 2024 20:35:55 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 31 Jan 2024 20:35:55 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 31 Jan 2024 20:35:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Jan 2024 20:35:56 GMT
EXPOSE 8529
# Wed, 31 Jan 2024 20:35:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d74030c339774749265793814eaf9cf91f7f83b95af4d85eb46624a6d0997f4`  
		Last Modified: Wed, 31 Jan 2024 20:36:32 GMT  
		Size: 222.8 MB (222831169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb609e1eadc96d222069b4e2506f5a02db98ca180811dc42fb899adf6b470a6e`  
		Last Modified: Wed, 31 Jan 2024 20:36:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ea17133aae1e830acd119ae8ded19e45e5470d1793ac79da1eba76c3a853e5`  
		Last Modified: Wed, 31 Jan 2024 20:36:09 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65234e47c6549027bc851130d713d887197486236e108fc1229a59824ff7f3a`  
		Last Modified: Wed, 31 Jan 2024 20:36:09 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:aea7f2471b3985a88ae1d363f45ed6f9b4ae8c2eb5ddfa0cda0c13f4743d2caa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220708421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc35170887585ba8bb1c16f02aa1600cda09c8812f24cae6823f827c0cab96df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:39:03 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 31 Jan 2024 20:45:03 GMT
ENV ARANGO_VERSION=3.10.13
# Wed, 31 Jan 2024 20:45:28 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 31 Jan 2024 20:45:32 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 31 Jan 2024 20:45:32 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 31 Jan 2024 20:45:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 31 Jan 2024 20:45:33 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 31 Jan 2024 20:45:33 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 31 Jan 2024 20:45:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Jan 2024 20:45:33 GMT
EXPOSE 8529
# Wed, 31 Jan 2024 20:45:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dbbecb279e0e3931a848e92e2ceff65d8d4bb2ec0ca0d9562f5c02a5eceb6`  
		Last Modified: Wed, 31 Jan 2024 20:46:27 GMT  
		Size: 218.0 MB (217997651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9382c2acdf95caec7fba141d80239c31558f4516b437dba5b53f6dd249c3d3`  
		Last Modified: Wed, 31 Jan 2024 20:45:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e345c905745441463cd2e0de8dd6e610afca6e37eeabf76e6a9ac497e3d010`  
		Last Modified: Wed, 31 Jan 2024 20:45:45 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0439b833b66c817b0e1e5fa9f878f36abc38ffb5b003fcc0b072907f35775b1`  
		Last Modified: Wed, 31 Jan 2024 20:45:45 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.10.13`

```console
$ docker pull arangodb@sha256:2fc2d3996cbb945647b793dd8e79950445fa7b90c9a99dbca59c8603114e82ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10.13` - linux; amd64

```console
$ docker pull arangodb@sha256:b671d8f118c7a6a9a1596f5f76fe80dd32d99e1b164f9e4cd042dd178adde57f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225641490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9dcd7adf87108998b35fd7b78799113a4c7fd138ae366d602534ba20f73780`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:33:45 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 31 Jan 2024 20:35:25 GMT
ENV ARANGO_VERSION=3.10.13
# Wed, 31 Jan 2024 20:35:53 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 31 Jan 2024 20:35:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 31 Jan 2024 20:35:55 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 31 Jan 2024 20:35:55 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 31 Jan 2024 20:35:55 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 31 Jan 2024 20:35:55 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 31 Jan 2024 20:35:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Jan 2024 20:35:56 GMT
EXPOSE 8529
# Wed, 31 Jan 2024 20:35:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d74030c339774749265793814eaf9cf91f7f83b95af4d85eb46624a6d0997f4`  
		Last Modified: Wed, 31 Jan 2024 20:36:32 GMT  
		Size: 222.8 MB (222831169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb609e1eadc96d222069b4e2506f5a02db98ca180811dc42fb899adf6b470a6e`  
		Last Modified: Wed, 31 Jan 2024 20:36:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ea17133aae1e830acd119ae8ded19e45e5470d1793ac79da1eba76c3a853e5`  
		Last Modified: Wed, 31 Jan 2024 20:36:09 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65234e47c6549027bc851130d713d887197486236e108fc1229a59824ff7f3a`  
		Last Modified: Wed, 31 Jan 2024 20:36:09 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10.13` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:aea7f2471b3985a88ae1d363f45ed6f9b4ae8c2eb5ddfa0cda0c13f4743d2caa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220708421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc35170887585ba8bb1c16f02aa1600cda09c8812f24cae6823f827c0cab96df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:39:03 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 31 Jan 2024 20:45:03 GMT
ENV ARANGO_VERSION=3.10.13
# Wed, 31 Jan 2024 20:45:28 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 31 Jan 2024 20:45:32 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 31 Jan 2024 20:45:32 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 31 Jan 2024 20:45:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 31 Jan 2024 20:45:33 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 31 Jan 2024 20:45:33 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 31 Jan 2024 20:45:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Jan 2024 20:45:33 GMT
EXPOSE 8529
# Wed, 31 Jan 2024 20:45:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dbbecb279e0e3931a848e92e2ceff65d8d4bb2ec0ca0d9562f5c02a5eceb6`  
		Last Modified: Wed, 31 Jan 2024 20:46:27 GMT  
		Size: 218.0 MB (217997651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9382c2acdf95caec7fba141d80239c31558f4516b437dba5b53f6dd249c3d3`  
		Last Modified: Wed, 31 Jan 2024 20:45:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e345c905745441463cd2e0de8dd6e610afca6e37eeabf76e6a9ac497e3d010`  
		Last Modified: Wed, 31 Jan 2024 20:45:45 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0439b833b66c817b0e1e5fa9f878f36abc38ffb5b003fcc0b072907f35775b1`  
		Last Modified: Wed, 31 Jan 2024 20:45:45 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:20d83df5f54962a08eb9de9132b7dc2da095cfb42d020e93ec3287ea1ac88089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:8dc99b915b8e0ca00c1b7f31e1945fd6aa653bdc28d0d4cd625c3b5d93bd06e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250210528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49a71d685d3be48256a5f3bd5f7ade67251d6ae4a2974a3066f52929365a227`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:33:45 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 06 Feb 2024 08:29:09 GMT
ENV ARANGO_VERSION=3.11.7
# Tue, 06 Feb 2024 08:29:36 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 06 Feb 2024 08:29:38 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 06 Feb 2024 08:29:38 GMT
RUN echo "UTC" > /etc/timezone
# Tue, 06 Feb 2024 08:29:38 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 06 Feb 2024 08:29:38 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 06 Feb 2024 08:29:39 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 06 Feb 2024 08:29:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Feb 2024 08:29:39 GMT
EXPOSE 8529
# Tue, 06 Feb 2024 08:29:39 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c7a04a6fbbaa061a335da6a2a549f2043ace27278401507130841c9c7461f`  
		Last Modified: Tue, 06 Feb 2024 08:30:14 GMT  
		Size: 247.4 MB (247400204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35ff609d377e9a129127852725984bb2e69001037b24c89a6b3372a4f3ef90b`  
		Last Modified: Tue, 06 Feb 2024 08:29:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1378ab7af0757bb6657db44eb3f9229f192b5f504bc98aeb36d9fbdf755f83ca`  
		Last Modified: Tue, 06 Feb 2024 08:29:51 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688a9e589bdb7bb927560034da35b59aa4bf96da2f688c7b1d5110e3b94d462b`  
		Last Modified: Tue, 06 Feb 2024 08:29:51 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.11` - linux; arm64 variant v8

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

## `arangodb:3.11.8`

```console
$ docker pull arangodb@sha256:fe4a61f8ad35a98aea58d506f134dd97699cfe37db662a1b10c283276684e921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `arangodb:3.11.8` - linux; arm64 variant v8

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

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:20d83df5f54962a08eb9de9132b7dc2da095cfb42d020e93ec3287ea1ac88089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:8dc99b915b8e0ca00c1b7f31e1945fd6aa653bdc28d0d4cd625c3b5d93bd06e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250210528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49a71d685d3be48256a5f3bd5f7ade67251d6ae4a2974a3066f52929365a227`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:33:45 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 06 Feb 2024 08:29:09 GMT
ENV ARANGO_VERSION=3.11.7
# Tue, 06 Feb 2024 08:29:36 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 06 Feb 2024 08:29:38 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 06 Feb 2024 08:29:38 GMT
RUN echo "UTC" > /etc/timezone
# Tue, 06 Feb 2024 08:29:38 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 06 Feb 2024 08:29:38 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 06 Feb 2024 08:29:39 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 06 Feb 2024 08:29:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Feb 2024 08:29:39 GMT
EXPOSE 8529
# Tue, 06 Feb 2024 08:29:39 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c7a04a6fbbaa061a335da6a2a549f2043ace27278401507130841c9c7461f`  
		Last Modified: Tue, 06 Feb 2024 08:30:14 GMT  
		Size: 247.4 MB (247400204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35ff609d377e9a129127852725984bb2e69001037b24c89a6b3372a4f3ef90b`  
		Last Modified: Tue, 06 Feb 2024 08:29:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1378ab7af0757bb6657db44eb3f9229f192b5f504bc98aeb36d9fbdf755f83ca`  
		Last Modified: Tue, 06 Feb 2024 08:29:51 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688a9e589bdb7bb927560034da35b59aa4bf96da2f688c7b1d5110e3b94d462b`  
		Last Modified: Tue, 06 Feb 2024 08:29:51 GMT  
		Size: 261.0 B  
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
