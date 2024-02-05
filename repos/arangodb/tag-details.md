<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.10`](#arangodb310)
-	[`arangodb:3.10.13`](#arangodb31013)
-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.7`](#arangodb3117)
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
$ docker pull arangodb@sha256:fe246b1f601b4b01bc5c9f91076a08e8f0fe8836c6a56a31353a1a46094a404e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:2926e176b0a7beda276b36ee2fb87d4352773986781f5ddf5eea1ef9db6097ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249761169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810210558f215fe40894c15384c7e2addef699415483684c261dad6e9c6c0dbd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:33:45 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 27 Jan 2024 03:34:20 GMT
ENV ARANGO_VERSION=3.11.6
# Sat, 27 Jan 2024 03:34:48 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 27 Jan 2024 03:34:50 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 27 Jan 2024 03:34:51 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 27 Jan 2024 03:34:51 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 27 Jan 2024 03:34:51 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:34:51 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 27 Jan 2024 03:34:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:34:51 GMT
EXPOSE 8529
# Sat, 27 Jan 2024 03:34:51 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7930f60bbebfc0dec4523c98e0635f857cd5fcfc613148657ddb94bf1d9889`  
		Last Modified: Sat, 27 Jan 2024 03:35:53 GMT  
		Size: 247.0 MB (246950845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1f643d3b38900faeb79ba64d5024fa893d0b37e06fa40f233498112541530a`  
		Last Modified: Sat, 27 Jan 2024 03:35:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e62839698b1d2f091be10c2a5225209efea9b8f09fdd075bf4b104fe54ae1a`  
		Last Modified: Sat, 27 Jan 2024 03:35:31 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb353e24fb5fa164f0fc90ffd39965944a0901dbdc3d20ed3b0a391763c2587`  
		Last Modified: Sat, 27 Jan 2024 03:35:31 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:32c89594c106f83b13257a8a57ce8948f994cd14568ad87df30291289c06fff8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243870267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d76f2163d78bf1b76f984ccce3eb05720722a482ed3998d57b56783e2e58b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:39:03 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 27 Jan 2024 00:39:43 GMT
ENV ARANGO_VERSION=3.11.6
# Sat, 27 Jan 2024 00:40:09 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 27 Jan 2024 00:40:16 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 27 Jan 2024 00:40:16 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 27 Jan 2024 00:40:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 27 Jan 2024 00:40:16 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 27 Jan 2024 00:40:16 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 27 Jan 2024 00:40:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 00:40:16 GMT
EXPOSE 8529
# Sat, 27 Jan 2024 00:40:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07811b3267ce79180a92736166e4a622fbc1f0b5614045d38608192ddf48b873`  
		Last Modified: Sat, 27 Jan 2024 00:41:12 GMT  
		Size: 241.2 MB (241159498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d038b17d31fbdf8b032e37b9857d47fafe15292c7dd1460e6f0112506636ad`  
		Last Modified: Sat, 27 Jan 2024 00:40:55 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec029480ad3deb03ebfa4b515f71da19cd238abf0f99f31e224b0ea4e0b74e6d`  
		Last Modified: Sat, 27 Jan 2024 00:40:55 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d172f68ba3795b2cf4ca72962dad22e0126dd213e169abe772ddea0615d5497`  
		Last Modified: Sat, 27 Jan 2024 00:40:55 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.11.7`

**does not exist** (yet?)

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:fe246b1f601b4b01bc5c9f91076a08e8f0fe8836c6a56a31353a1a46094a404e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:2926e176b0a7beda276b36ee2fb87d4352773986781f5ddf5eea1ef9db6097ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249761169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810210558f215fe40894c15384c7e2addef699415483684c261dad6e9c6c0dbd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:33:45 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 27 Jan 2024 03:34:20 GMT
ENV ARANGO_VERSION=3.11.6
# Sat, 27 Jan 2024 03:34:48 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 27 Jan 2024 03:34:50 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 27 Jan 2024 03:34:51 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 27 Jan 2024 03:34:51 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 27 Jan 2024 03:34:51 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:34:51 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 27 Jan 2024 03:34:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:34:51 GMT
EXPOSE 8529
# Sat, 27 Jan 2024 03:34:51 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7930f60bbebfc0dec4523c98e0635f857cd5fcfc613148657ddb94bf1d9889`  
		Last Modified: Sat, 27 Jan 2024 03:35:53 GMT  
		Size: 247.0 MB (246950845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1f643d3b38900faeb79ba64d5024fa893d0b37e06fa40f233498112541530a`  
		Last Modified: Sat, 27 Jan 2024 03:35:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e62839698b1d2f091be10c2a5225209efea9b8f09fdd075bf4b104fe54ae1a`  
		Last Modified: Sat, 27 Jan 2024 03:35:31 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb353e24fb5fa164f0fc90ffd39965944a0901dbdc3d20ed3b0a391763c2587`  
		Last Modified: Sat, 27 Jan 2024 03:35:31 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:32c89594c106f83b13257a8a57ce8948f994cd14568ad87df30291289c06fff8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243870267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d76f2163d78bf1b76f984ccce3eb05720722a482ed3998d57b56783e2e58b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:39:03 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 27 Jan 2024 00:39:43 GMT
ENV ARANGO_VERSION=3.11.6
# Sat, 27 Jan 2024 00:40:09 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 27 Jan 2024 00:40:16 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 27 Jan 2024 00:40:16 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 27 Jan 2024 00:40:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 27 Jan 2024 00:40:16 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 27 Jan 2024 00:40:16 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 27 Jan 2024 00:40:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 00:40:16 GMT
EXPOSE 8529
# Sat, 27 Jan 2024 00:40:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07811b3267ce79180a92736166e4a622fbc1f0b5614045d38608192ddf48b873`  
		Last Modified: Sat, 27 Jan 2024 00:41:12 GMT  
		Size: 241.2 MB (241159498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d038b17d31fbdf8b032e37b9857d47fafe15292c7dd1460e6f0112506636ad`  
		Last Modified: Sat, 27 Jan 2024 00:40:55 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec029480ad3deb03ebfa4b515f71da19cd238abf0f99f31e224b0ea4e0b74e6d`  
		Last Modified: Sat, 27 Jan 2024 00:40:55 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d172f68ba3795b2cf4ca72962dad22e0126dd213e169abe772ddea0615d5497`  
		Last Modified: Sat, 27 Jan 2024 00:40:55 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
