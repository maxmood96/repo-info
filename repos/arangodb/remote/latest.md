## `arangodb:latest`

```console
$ docker pull arangodb@sha256:8fd9123f7ce6f75efc62b8e94edb06f7a8b738c94996d94b8fd27de0fa965150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:999b44ca9d70b7beae9b51aec9da16c4c9daf77283d8c3f291fc6c850321a741
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 MB (218887650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7c720d994f4adf1a4287db33da9e9a83918c86dc41154af3f4fedc7edd83a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 12 Oct 2022 19:19:28 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 10 Nov 2022 20:20:48 GMT
ENV ARANGO_VERSION=3.10.1
# Thu, 10 Nov 2022 20:21:14 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.0 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 10 Nov 2022 20:21:15 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 10 Nov 2022 20:21:16 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 10 Nov 2022 20:21:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 10 Nov 2022 20:21:16 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 10 Nov 2022 20:21:16 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 10 Nov 2022 20:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Nov 2022 20:21:17 GMT
EXPOSE 8529
# Thu, 10 Nov 2022 20:21:17 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f8096fce9f3584b0e9fcea1c87d294760695ae7b52926a81b2723656a1c0ca`  
		Last Modified: Thu, 10 Nov 2022 20:21:58 GMT  
		Size: 216.1 MB (216079109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5044b000c08463ffd9330c0fa80421c6b48588fc95496a2213db4043af2037e`  
		Last Modified: Thu, 10 Nov 2022 20:21:34 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb722b98beeec30fbdcd94f32cbfecb53bb1c73ded621fee2bd0d67980a2af8f`  
		Last Modified: Thu, 10 Nov 2022 20:21:34 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd387c6e50f5af0ee466e0219ab7db7e2989e271c3a6b509574bb7550535dbf`  
		Last Modified: Thu, 10 Nov 2022 20:21:34 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:bfe2bad277d6194cd6582fd161566ba6a98f7803b15a9001cdd1fc2839c5d46e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213568318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4884ff439d28dc68edec3a8163ca6041b10ff8423ba67f3a3483a42d16947696`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Thu, 10 Nov 2022 20:39:41 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 20:40:58 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 10 Nov 2022 20:40:58 GMT
ENV ARANGO_VERSION=3.10.1
# Thu, 10 Nov 2022 20:41:20 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.0 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 10 Nov 2022 20:41:24 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 10 Nov 2022 20:41:24 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 10 Nov 2022 20:41:24 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 10 Nov 2022 20:41:24 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 10 Nov 2022 20:41:24 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 10 Nov 2022 20:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Nov 2022 20:41:24 GMT
EXPOSE 8529
# Thu, 10 Nov 2022 20:41:25 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfb7eac48ceea29733e97df0512693e4c05262fc011d9b6b3211af125aa80ea`  
		Last Modified: Thu, 10 Nov 2022 20:41:55 GMT  
		Size: 210.9 MB (210858170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851154154cfb3d094e323035795d15f09ff139c8ee998bfaba4549bcaf180ea4`  
		Last Modified: Thu, 10 Nov 2022 20:41:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cbab6db577b2b8a94027d1286ffb2858c8df3114226aec44b0a4ae1d2aa50f`  
		Last Modified: Thu, 10 Nov 2022 20:41:38 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b46638b706329a23745fbdfb4d4330bc911a0dfb8143467a9be9f56cffaa76`  
		Last Modified: Thu, 10 Nov 2022 20:41:37 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
