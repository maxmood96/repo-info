<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.4`](#arangodb34)
-	[`arangodb:3.4.10`](#arangodb3410)
-	[`arangodb:3.5`](#arangodb35)
-	[`arangodb:3.5.5`](#arangodb355)
-	[`arangodb:3.6`](#arangodb36)
-	[`arangodb:3.6.5`](#arangodb365)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.4`

```console
$ docker pull arangodb@sha256:0021d43dd41f858281433f4a9355126073bf8db13ff0113a3ca63b94fd33664d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.4` - linux; amd64

```console
$ docker pull arangodb@sha256:a91670c79cd10bf5c4c01050a1f47c77db047cdbe3897f498f391a3378375af1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101998675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ece3b9e98068925171fa1f7264648009ca3bc12fb3ecf134b46cae7d41041e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:25:39 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 07 May 2020 23:19:23 GMT
ENV ARANGO_VERSION=3.4.10
# Thu, 07 May 2020 23:19:24 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64
# Thu, 07 May 2020 23:19:24 GMT
ENV ARANGO_PACKAGE=arangodb3_3.4.10-1_amd64.deb
# Thu, 07 May 2020 23:19:24 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64/arangodb3_3.4.10-1_amd64.deb
# Thu, 07 May 2020 23:19:24 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64/arangodb3_3.4.10-1_amd64.deb.asc
# Tue, 21 Jul 2020 00:19:46 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl &&     npm install -g foxx-cli@1.3.0 &&     rm -rf /root/.npm &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 21 Jul 2020 00:19:47 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 21 Jul 2020 00:19:47 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Tue, 21 Jul 2020 00:19:47 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Tue, 21 Jul 2020 00:19:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Jul 2020 00:19:48 GMT
EXPOSE 8529
# Tue, 21 Jul 2020 00:19:48 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f554909152e5f5223bf65bef82c5fc32be5d66541446142a8a9ce167971afbb1`  
		Last Modified: Tue, 21 Jul 2020 00:21:26 GMT  
		Size: 99.2 MB (99200648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89682fbf33f1cb7acde62f253fa33d0bde3db644089f76bf3c6986c81f0cf1c`  
		Last Modified: Tue, 21 Jul 2020 00:21:08 GMT  
		Size: 2.2 KB (2205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070420db5948a411353e8240dae706d47805ad914df881089356c92a5b0eba1c`  
		Last Modified: Tue, 21 Jul 2020 00:21:08 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.4.10`

```console
$ docker pull arangodb@sha256:0021d43dd41f858281433f4a9355126073bf8db13ff0113a3ca63b94fd33664d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.4.10` - linux; amd64

```console
$ docker pull arangodb@sha256:a91670c79cd10bf5c4c01050a1f47c77db047cdbe3897f498f391a3378375af1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101998675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ece3b9e98068925171fa1f7264648009ca3bc12fb3ecf134b46cae7d41041e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:25:39 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 07 May 2020 23:19:23 GMT
ENV ARANGO_VERSION=3.4.10
# Thu, 07 May 2020 23:19:24 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64
# Thu, 07 May 2020 23:19:24 GMT
ENV ARANGO_PACKAGE=arangodb3_3.4.10-1_amd64.deb
# Thu, 07 May 2020 23:19:24 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64/arangodb3_3.4.10-1_amd64.deb
# Thu, 07 May 2020 23:19:24 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64/arangodb3_3.4.10-1_amd64.deb.asc
# Tue, 21 Jul 2020 00:19:46 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl &&     npm install -g foxx-cli@1.3.0 &&     rm -rf /root/.npm &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 21 Jul 2020 00:19:47 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 21 Jul 2020 00:19:47 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Tue, 21 Jul 2020 00:19:47 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Tue, 21 Jul 2020 00:19:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Jul 2020 00:19:48 GMT
EXPOSE 8529
# Tue, 21 Jul 2020 00:19:48 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f554909152e5f5223bf65bef82c5fc32be5d66541446142a8a9ce167971afbb1`  
		Last Modified: Tue, 21 Jul 2020 00:21:26 GMT  
		Size: 99.2 MB (99200648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89682fbf33f1cb7acde62f253fa33d0bde3db644089f76bf3c6986c81f0cf1c`  
		Last Modified: Tue, 21 Jul 2020 00:21:08 GMT  
		Size: 2.2 KB (2205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070420db5948a411353e8240dae706d47805ad914df881089356c92a5b0eba1c`  
		Last Modified: Tue, 21 Jul 2020 00:21:08 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.5`

```console
$ docker pull arangodb@sha256:60faf3c6fd35755b80877275151d12f591f06431fdb0b2d00a9924d78c405c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.5` - linux; amd64

```console
$ docker pull arangodb@sha256:d4f862c2c0d2b8de69490b38f4c615701b280baac94150b0852f9b34ceed49aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110863375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6f3a99bd89f6f3c8ae1ed7b18c4e6eb9a125f591bfb97fd5b9b10627cdba11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:25:39 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 11 May 2020 15:20:31 GMT
ENV ARANGO_VERSION=3.5.5.1
# Mon, 11 May 2020 15:20:31 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64
# Mon, 11 May 2020 15:20:31 GMT
ENV ARANGO_PACKAGE=arangodb3_3.5.5.1-1_amd64.deb
# Mon, 11 May 2020 15:20:31 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.5.1-1_amd64.deb
# Mon, 11 May 2020 15:20:31 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.5.1-1_amd64.deb.asc
# Tue, 21 Jul 2020 00:20:16 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl numactl-tools &&     npm install -g foxx-cli@1.3.0 &&     rm -rf /root/.npm &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 21 Jul 2020 00:20:17 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 21 Jul 2020 00:20:18 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Tue, 21 Jul 2020 00:20:19 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Tue, 21 Jul 2020 00:20:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Jul 2020 00:20:19 GMT
EXPOSE 8529
# Tue, 21 Jul 2020 00:20:20 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da11ab3986ac732a8dcd9d6f4c3949957af35dd93edccd0a18a60b966f589420`  
		Last Modified: Tue, 21 Jul 2020 00:21:51 GMT  
		Size: 108.1 MB (108065346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3c2e0cb457f1f8e92a66b3f52f242d2423cea7b0b52855a8ebce7dbc16a4d3`  
		Last Modified: Tue, 21 Jul 2020 00:21:33 GMT  
		Size: 2.2 KB (2205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d08679e63a0890b3d611830208b9de4ab4f8fa07e0a458f4ce900241295800`  
		Last Modified: Tue, 21 Jul 2020 00:21:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.5.5`

```console
$ docker pull arangodb@sha256:60faf3c6fd35755b80877275151d12f591f06431fdb0b2d00a9924d78c405c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.5.5` - linux; amd64

```console
$ docker pull arangodb@sha256:d4f862c2c0d2b8de69490b38f4c615701b280baac94150b0852f9b34ceed49aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110863375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6f3a99bd89f6f3c8ae1ed7b18c4e6eb9a125f591bfb97fd5b9b10627cdba11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:25:39 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 11 May 2020 15:20:31 GMT
ENV ARANGO_VERSION=3.5.5.1
# Mon, 11 May 2020 15:20:31 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64
# Mon, 11 May 2020 15:20:31 GMT
ENV ARANGO_PACKAGE=arangodb3_3.5.5.1-1_amd64.deb
# Mon, 11 May 2020 15:20:31 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.5.1-1_amd64.deb
# Mon, 11 May 2020 15:20:31 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.5.1-1_amd64.deb.asc
# Tue, 21 Jul 2020 00:20:16 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl numactl-tools &&     npm install -g foxx-cli@1.3.0 &&     rm -rf /root/.npm &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 21 Jul 2020 00:20:17 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 21 Jul 2020 00:20:18 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Tue, 21 Jul 2020 00:20:19 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Tue, 21 Jul 2020 00:20:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Jul 2020 00:20:19 GMT
EXPOSE 8529
# Tue, 21 Jul 2020 00:20:20 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da11ab3986ac732a8dcd9d6f4c3949957af35dd93edccd0a18a60b966f589420`  
		Last Modified: Tue, 21 Jul 2020 00:21:51 GMT  
		Size: 108.1 MB (108065346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3c2e0cb457f1f8e92a66b3f52f242d2423cea7b0b52855a8ebce7dbc16a4d3`  
		Last Modified: Tue, 21 Jul 2020 00:21:33 GMT  
		Size: 2.2 KB (2205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d08679e63a0890b3d611830208b9de4ab4f8fa07e0a458f4ce900241295800`  
		Last Modified: Tue, 21 Jul 2020 00:21:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.6`

```console
$ docker pull arangodb@sha256:6007c1d9537e37f38ab3adeb3c4530166f579b61599111e121bdca8b2bab9b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.6` - linux; amd64

```console
$ docker pull arangodb@sha256:fdba9acc2975d3bf9260aad9bd7504926b4664d480b8bb789ff31ce3e2f9a2b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107140365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17257d7ca195af9046b77dbadf643d2b9afe980e051e107fcd761246898ef63a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:25:39 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 21 Jul 2020 00:20:26 GMT
ENV ARANGO_VERSION=3.6.5
# Tue, 21 Jul 2020 00:20:27 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Tue, 21 Jul 2020 00:20:27 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.5-1_amd64.deb
# Tue, 21 Jul 2020 00:20:27 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.5-1_amd64.deb
# Tue, 21 Jul 2020 00:20:27 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.5-1_amd64.deb.asc
# Tue, 21 Jul 2020 00:20:51 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     apk add --no-cache --repository http://dl-cdn.alpinelinux.org/alpine/v3.11/main/ nodejs npm &&     npm install -g foxx-cli &&     rm -rf /root/.npm && apk del npm &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 21 Jul 2020 00:20:51 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 21 Jul 2020 00:20:52 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Tue, 21 Jul 2020 00:20:52 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Tue, 21 Jul 2020 00:20:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Jul 2020 00:20:52 GMT
EXPOSE 8529
# Tue, 21 Jul 2020 00:20:52 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33254baf3c1734db37e62edb8e2e7b834b00b816dfc54ef15f89f57857819cc`  
		Last Modified: Tue, 21 Jul 2020 00:22:13 GMT  
		Size: 104.3 MB (104342338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11538a2692c1f62be4010657585a47bfda0cac63830a405440771cbeb5c32fd0`  
		Last Modified: Tue, 21 Jul 2020 00:21:56 GMT  
		Size: 2.2 KB (2205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ad1149e5ca941131e4c39a36f651d42f68886bdc5edc879ca536ea995e607f`  
		Last Modified: Tue, 21 Jul 2020 00:21:56 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.6.5`

```console
$ docker pull arangodb@sha256:6007c1d9537e37f38ab3adeb3c4530166f579b61599111e121bdca8b2bab9b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.6.5` - linux; amd64

```console
$ docker pull arangodb@sha256:fdba9acc2975d3bf9260aad9bd7504926b4664d480b8bb789ff31ce3e2f9a2b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107140365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17257d7ca195af9046b77dbadf643d2b9afe980e051e107fcd761246898ef63a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:25:39 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 21 Jul 2020 00:20:26 GMT
ENV ARANGO_VERSION=3.6.5
# Tue, 21 Jul 2020 00:20:27 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Tue, 21 Jul 2020 00:20:27 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.5-1_amd64.deb
# Tue, 21 Jul 2020 00:20:27 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.5-1_amd64.deb
# Tue, 21 Jul 2020 00:20:27 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.5-1_amd64.deb.asc
# Tue, 21 Jul 2020 00:20:51 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     apk add --no-cache --repository http://dl-cdn.alpinelinux.org/alpine/v3.11/main/ nodejs npm &&     npm install -g foxx-cli &&     rm -rf /root/.npm && apk del npm &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 21 Jul 2020 00:20:51 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 21 Jul 2020 00:20:52 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Tue, 21 Jul 2020 00:20:52 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Tue, 21 Jul 2020 00:20:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Jul 2020 00:20:52 GMT
EXPOSE 8529
# Tue, 21 Jul 2020 00:20:52 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33254baf3c1734db37e62edb8e2e7b834b00b816dfc54ef15f89f57857819cc`  
		Last Modified: Tue, 21 Jul 2020 00:22:13 GMT  
		Size: 104.3 MB (104342338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11538a2692c1f62be4010657585a47bfda0cac63830a405440771cbeb5c32fd0`  
		Last Modified: Tue, 21 Jul 2020 00:21:56 GMT  
		Size: 2.2 KB (2205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ad1149e5ca941131e4c39a36f651d42f68886bdc5edc879ca536ea995e607f`  
		Last Modified: Tue, 21 Jul 2020 00:21:56 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:6007c1d9537e37f38ab3adeb3c4530166f579b61599111e121bdca8b2bab9b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:fdba9acc2975d3bf9260aad9bd7504926b4664d480b8bb789ff31ce3e2f9a2b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107140365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17257d7ca195af9046b77dbadf643d2b9afe980e051e107fcd761246898ef63a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:25:39 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 21 Jul 2020 00:20:26 GMT
ENV ARANGO_VERSION=3.6.5
# Tue, 21 Jul 2020 00:20:27 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Tue, 21 Jul 2020 00:20:27 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.5-1_amd64.deb
# Tue, 21 Jul 2020 00:20:27 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.5-1_amd64.deb
# Tue, 21 Jul 2020 00:20:27 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.5-1_amd64.deb.asc
# Tue, 21 Jul 2020 00:20:51 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     apk add --no-cache --repository http://dl-cdn.alpinelinux.org/alpine/v3.11/main/ nodejs npm &&     npm install -g foxx-cli &&     rm -rf /root/.npm && apk del npm &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 21 Jul 2020 00:20:51 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 21 Jul 2020 00:20:52 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Tue, 21 Jul 2020 00:20:52 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Tue, 21 Jul 2020 00:20:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Jul 2020 00:20:52 GMT
EXPOSE 8529
# Tue, 21 Jul 2020 00:20:52 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33254baf3c1734db37e62edb8e2e7b834b00b816dfc54ef15f89f57857819cc`  
		Last Modified: Tue, 21 Jul 2020 00:22:13 GMT  
		Size: 104.3 MB (104342338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11538a2692c1f62be4010657585a47bfda0cac63830a405440771cbeb5c32fd0`  
		Last Modified: Tue, 21 Jul 2020 00:21:56 GMT  
		Size: 2.2 KB (2205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ad1149e5ca941131e4c39a36f651d42f68886bdc5edc879ca536ea995e607f`  
		Last Modified: Tue, 21 Jul 2020 00:21:56 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
