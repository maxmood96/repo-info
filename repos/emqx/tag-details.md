<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.4`](#emqx584)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:a3c253ea20230ff42b9f882b0d605ef595a6ea55432b057b1702412d87afbbba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:3e5405dfffaf421571a1c8e14363e9adc41192cd86117190694de42742092cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105350410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55329d10b3f3b619a907422433e2c75b5bd0e0702ef9ee5985a2256714cb314`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ceb8aafe9c77e86d2521700d454ad8ae4387401367949ca90613c76b91df7f`  
		Last Modified: Tue, 14 Jan 2025 20:50:39 GMT  
		Size: 77.1 MB (77136933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e979a3de595b84c17e74b35087195dee7c6e6b888c95b9b3b1590cb5ff10baf5`  
		Last Modified: Tue, 14 Jan 2025 20:53:34 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:bc1ca923683881c335c427137c0dd34f0d729a74dd9cbd0496afe1f337dce3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd4e8b718a636343850542367c3b8ff0c314abc8294808b1f334023dc645cdf`

```dockerfile
```

-	Layers:
	-	`sha256:3c4b62aae98ccc4891811eb92a9e3bcd5ab16587121947cd2f87e6eedb469c6c`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 2.6 MB (2614482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a28dc4943612997fc595414de42efdbf37fc03d31749c97e7d4d00700aec50`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8d3305abc33a18d1db2186ba85a1728dd9ee8b6a703b9d605ee593a9b6635206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102450607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a4611268228c1ec582b521138dcb3c845bdce7fa1381b22a39c255d5ff7e28`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cf553a1d689590ff4987101df413b6286a024eb13d9a13ad65e42a1999caff`  
		Last Modified: Tue, 14 Jan 2025 02:27:20 GMT  
		Size: 74.4 MB (74408514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df10519d0232bec08057b71fd3704f520f7da59f5e891731e021b62b3d10eb2e`  
		Last Modified: Tue, 14 Jan 2025 21:01:34 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:a56a1d194261b6e166f83e557e6e246e652542dd58c4544790a8c500318493b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d851a39eebad7d5543766ae04846fa07dcc4ce1df5329b3c6691a485681d7e`

```dockerfile
```

-	Layers:
	-	`sha256:194ab48a6e69122107093a054875cd870fd510d4847e6e8d47c373fc421bf232`  
		Last Modified: Tue, 14 Jan 2025 02:27:18 GMT  
		Size: 2.6 MB (2614762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc1f0ddfa38dd63521376d39ae56d217882859d1bf4716917e5524591bec9393`  
		Last Modified: Tue, 14 Jan 2025 02:27:17 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:85cc7a4417c259429f4acc88dea66b558206e7ee747fd31c6af31d4ef470a7eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:1c5fc1fe9978edb9176c100692bff7be85c4ee675c3bf4aabca14c3cad28bf33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125361343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4251dc9adeaae2dae4e35e781112b5b86cac9c487218b53fab156e5695041bd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 12 Aug 2024 08:39:51 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 12 Aug 2024 08:39:51 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 12 Aug 2024 08:39:51 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 12 Aug 2024 08:39:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 12 Aug 2024 08:39:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
WORKDIR /opt/emqx
# Mon, 12 Aug 2024 08:39:51 GMT
USER emqx
# Mon, 12 Aug 2024 08:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 12 Aug 2024 08:39:51 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 12 Aug 2024 08:39:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffebec81205837a619f24d9d52aad550aae2ce732d91aacd169b6817ad81f36`  
		Last Modified: Tue, 14 Jan 2025 22:26:31 GMT  
		Size: 97.1 MB (97147866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4d653f2bc98e478d8d2c32472536a87d7919ad30ccec8b67c24a92e6907b35`  
		Last Modified: Tue, 14 Jan 2025 02:15:59 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:d9c5bd315d3b4d85e2436aa8270cb5493a7431b3396185a0c72afbbbf6753cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df6126bacb4ee88fdbf6e53dee5ce05e9fa05f587021d0eae70bc4dcecc283f`

```dockerfile
```

-	Layers:
	-	`sha256:938ba604990d8de87c1499bcc4053d75ee60a22d3a2df3f1a09e753898b1255d`  
		Last Modified: Tue, 14 Jan 2025 02:15:59 GMT  
		Size: 2.6 MB (2623881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3448dd913422d5bd0b9a6dc5c4b9e7ddacbd5f0294b19f21fec2307f4ee1b34`  
		Last Modified: Tue, 14 Jan 2025 02:15:59 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:26f1464b5b6fa3da0daebe41cc5c2db3d2de95adc1720db754c37d6e328d1c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121737698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaa52d7e2b53ef5102e1adf3a535300be05f68c9a55e565bb3bebbe50730d4d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 12 Aug 2024 08:39:51 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 12 Aug 2024 08:39:51 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 12 Aug 2024 08:39:51 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 12 Aug 2024 08:39:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 12 Aug 2024 08:39:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
WORKDIR /opt/emqx
# Mon, 12 Aug 2024 08:39:51 GMT
USER emqx
# Mon, 12 Aug 2024 08:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 12 Aug 2024 08:39:51 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 12 Aug 2024 08:39:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33257671e0c6361095cc2826c958bc366c2077292a072fd3bee8e4c3acce87b5`  
		Last Modified: Tue, 14 Jan 2025 02:26:47 GMT  
		Size: 93.7 MB (93695605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cc0070d53afa046fb3fc3713796cbbb394313497a1bd0b107fb1ec4ff4bcac`  
		Last Modified: Tue, 14 Jan 2025 23:19:51 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:7040c252bfd70ab90188ec6f5de8c8de5025359cc44c94e4499f4a07af664553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5763225bd06e30701f594de834c8f117db358c1263008d16a4a3342b3f37a61e`

```dockerfile
```

-	Layers:
	-	`sha256:05553bc17ff3472ba8fcbfa8d181f6a3708ec0465f035985e5c84f62b3145c3a`  
		Last Modified: Tue, 14 Jan 2025 02:26:45 GMT  
		Size: 2.6 MB (2624137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ec01091bf3fce2bcd17ea8b0a617affcc00eca46a86aaff56a1c5e451524c0c`  
		Last Modified: Tue, 14 Jan 2025 02:26:45 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:85cc7a4417c259429f4acc88dea66b558206e7ee747fd31c6af31d4ef470a7eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:1c5fc1fe9978edb9176c100692bff7be85c4ee675c3bf4aabca14c3cad28bf33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125361343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4251dc9adeaae2dae4e35e781112b5b86cac9c487218b53fab156e5695041bd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 12 Aug 2024 08:39:51 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 12 Aug 2024 08:39:51 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 12 Aug 2024 08:39:51 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 12 Aug 2024 08:39:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 12 Aug 2024 08:39:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
WORKDIR /opt/emqx
# Mon, 12 Aug 2024 08:39:51 GMT
USER emqx
# Mon, 12 Aug 2024 08:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 12 Aug 2024 08:39:51 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 12 Aug 2024 08:39:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffebec81205837a619f24d9d52aad550aae2ce732d91aacd169b6817ad81f36`  
		Last Modified: Tue, 14 Jan 2025 22:26:31 GMT  
		Size: 97.1 MB (97147866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4d653f2bc98e478d8d2c32472536a87d7919ad30ccec8b67c24a92e6907b35`  
		Last Modified: Tue, 14 Jan 2025 02:15:59 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:d9c5bd315d3b4d85e2436aa8270cb5493a7431b3396185a0c72afbbbf6753cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df6126bacb4ee88fdbf6e53dee5ce05e9fa05f587021d0eae70bc4dcecc283f`

```dockerfile
```

-	Layers:
	-	`sha256:938ba604990d8de87c1499bcc4053d75ee60a22d3a2df3f1a09e753898b1255d`  
		Last Modified: Tue, 14 Jan 2025 02:15:59 GMT  
		Size: 2.6 MB (2623881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3448dd913422d5bd0b9a6dc5c4b9e7ddacbd5f0294b19f21fec2307f4ee1b34`  
		Last Modified: Tue, 14 Jan 2025 02:15:59 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:26f1464b5b6fa3da0daebe41cc5c2db3d2de95adc1720db754c37d6e328d1c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121737698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaa52d7e2b53ef5102e1adf3a535300be05f68c9a55e565bb3bebbe50730d4d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 12 Aug 2024 08:39:51 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 12 Aug 2024 08:39:51 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 12 Aug 2024 08:39:51 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 12 Aug 2024 08:39:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 12 Aug 2024 08:39:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
WORKDIR /opt/emqx
# Mon, 12 Aug 2024 08:39:51 GMT
USER emqx
# Mon, 12 Aug 2024 08:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 12 Aug 2024 08:39:51 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 12 Aug 2024 08:39:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33257671e0c6361095cc2826c958bc366c2077292a072fd3bee8e4c3acce87b5`  
		Last Modified: Tue, 14 Jan 2025 02:26:47 GMT  
		Size: 93.7 MB (93695605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cc0070d53afa046fb3fc3713796cbbb394313497a1bd0b107fb1ec4ff4bcac`  
		Last Modified: Tue, 14 Jan 2025 23:19:51 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:7040c252bfd70ab90188ec6f5de8c8de5025359cc44c94e4499f4a07af664553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5763225bd06e30701f594de834c8f117db358c1263008d16a4a3342b3f37a61e`

```dockerfile
```

-	Layers:
	-	`sha256:05553bc17ff3472ba8fcbfa8d181f6a3708ec0465f035985e5c84f62b3145c3a`  
		Last Modified: Tue, 14 Jan 2025 02:26:45 GMT  
		Size: 2.6 MB (2624137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ec01091bf3fce2bcd17ea8b0a617affcc00eca46a86aaff56a1c5e451524c0c`  
		Last Modified: Tue, 14 Jan 2025 02:26:45 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:a3c253ea20230ff42b9f882b0d605ef595a6ea55432b057b1702412d87afbbba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:3e5405dfffaf421571a1c8e14363e9adc41192cd86117190694de42742092cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105350410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55329d10b3f3b619a907422433e2c75b5bd0e0702ef9ee5985a2256714cb314`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ceb8aafe9c77e86d2521700d454ad8ae4387401367949ca90613c76b91df7f`  
		Last Modified: Tue, 14 Jan 2025 20:50:39 GMT  
		Size: 77.1 MB (77136933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e979a3de595b84c17e74b35087195dee7c6e6b888c95b9b3b1590cb5ff10baf5`  
		Last Modified: Tue, 14 Jan 2025 20:53:34 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:bc1ca923683881c335c427137c0dd34f0d729a74dd9cbd0496afe1f337dce3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd4e8b718a636343850542367c3b8ff0c314abc8294808b1f334023dc645cdf`

```dockerfile
```

-	Layers:
	-	`sha256:3c4b62aae98ccc4891811eb92a9e3bcd5ab16587121947cd2f87e6eedb469c6c`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 2.6 MB (2614482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a28dc4943612997fc595414de42efdbf37fc03d31749c97e7d4d00700aec50`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8d3305abc33a18d1db2186ba85a1728dd9ee8b6a703b9d605ee593a9b6635206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102450607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a4611268228c1ec582b521138dcb3c845bdce7fa1381b22a39c255d5ff7e28`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cf553a1d689590ff4987101df413b6286a024eb13d9a13ad65e42a1999caff`  
		Last Modified: Tue, 14 Jan 2025 02:27:20 GMT  
		Size: 74.4 MB (74408514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df10519d0232bec08057b71fd3704f520f7da59f5e891731e021b62b3d10eb2e`  
		Last Modified: Tue, 14 Jan 2025 21:01:34 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:a56a1d194261b6e166f83e557e6e246e652542dd58c4544790a8c500318493b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d851a39eebad7d5543766ae04846fa07dcc4ce1df5329b3c6691a485681d7e`

```dockerfile
```

-	Layers:
	-	`sha256:194ab48a6e69122107093a054875cd870fd510d4847e6e8d47c373fc421bf232`  
		Last Modified: Tue, 14 Jan 2025 02:27:18 GMT  
		Size: 2.6 MB (2614762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc1f0ddfa38dd63521376d39ae56d217882859d1bf4716917e5524591bec9393`  
		Last Modified: Tue, 14 Jan 2025 02:27:17 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.4`

```console
$ docker pull emqx@sha256:a3c253ea20230ff42b9f882b0d605ef595a6ea55432b057b1702412d87afbbba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.4` - linux; amd64

```console
$ docker pull emqx@sha256:3e5405dfffaf421571a1c8e14363e9adc41192cd86117190694de42742092cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105350410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55329d10b3f3b619a907422433e2c75b5bd0e0702ef9ee5985a2256714cb314`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ceb8aafe9c77e86d2521700d454ad8ae4387401367949ca90613c76b91df7f`  
		Last Modified: Tue, 14 Jan 2025 20:50:39 GMT  
		Size: 77.1 MB (77136933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e979a3de595b84c17e74b35087195dee7c6e6b888c95b9b3b1590cb5ff10baf5`  
		Last Modified: Tue, 14 Jan 2025 20:53:34 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.4` - unknown; unknown

```console
$ docker pull emqx@sha256:bc1ca923683881c335c427137c0dd34f0d729a74dd9cbd0496afe1f337dce3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd4e8b718a636343850542367c3b8ff0c314abc8294808b1f334023dc645cdf`

```dockerfile
```

-	Layers:
	-	`sha256:3c4b62aae98ccc4891811eb92a9e3bcd5ab16587121947cd2f87e6eedb469c6c`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 2.6 MB (2614482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a28dc4943612997fc595414de42efdbf37fc03d31749c97e7d4d00700aec50`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8d3305abc33a18d1db2186ba85a1728dd9ee8b6a703b9d605ee593a9b6635206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102450607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a4611268228c1ec582b521138dcb3c845bdce7fa1381b22a39c255d5ff7e28`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cf553a1d689590ff4987101df413b6286a024eb13d9a13ad65e42a1999caff`  
		Last Modified: Tue, 14 Jan 2025 02:27:20 GMT  
		Size: 74.4 MB (74408514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df10519d0232bec08057b71fd3704f520f7da59f5e891731e021b62b3d10eb2e`  
		Last Modified: Tue, 14 Jan 2025 21:01:34 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.4` - unknown; unknown

```console
$ docker pull emqx@sha256:a56a1d194261b6e166f83e557e6e246e652542dd58c4544790a8c500318493b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d851a39eebad7d5543766ae04846fa07dcc4ce1df5329b3c6691a485681d7e`

```dockerfile
```

-	Layers:
	-	`sha256:194ab48a6e69122107093a054875cd870fd510d4847e6e8d47c373fc421bf232`  
		Last Modified: Tue, 14 Jan 2025 02:27:18 GMT  
		Size: 2.6 MB (2614762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc1f0ddfa38dd63521376d39ae56d217882859d1bf4716917e5524591bec9393`  
		Last Modified: Tue, 14 Jan 2025 02:27:17 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:a3c253ea20230ff42b9f882b0d605ef595a6ea55432b057b1702412d87afbbba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:3e5405dfffaf421571a1c8e14363e9adc41192cd86117190694de42742092cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105350410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55329d10b3f3b619a907422433e2c75b5bd0e0702ef9ee5985a2256714cb314`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ceb8aafe9c77e86d2521700d454ad8ae4387401367949ca90613c76b91df7f`  
		Last Modified: Tue, 14 Jan 2025 20:50:39 GMT  
		Size: 77.1 MB (77136933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e979a3de595b84c17e74b35087195dee7c6e6b888c95b9b3b1590cb5ff10baf5`  
		Last Modified: Tue, 14 Jan 2025 20:53:34 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:bc1ca923683881c335c427137c0dd34f0d729a74dd9cbd0496afe1f337dce3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd4e8b718a636343850542367c3b8ff0c314abc8294808b1f334023dc645cdf`

```dockerfile
```

-	Layers:
	-	`sha256:3c4b62aae98ccc4891811eb92a9e3bcd5ab16587121947cd2f87e6eedb469c6c`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 2.6 MB (2614482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a28dc4943612997fc595414de42efdbf37fc03d31749c97e7d4d00700aec50`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8d3305abc33a18d1db2186ba85a1728dd9ee8b6a703b9d605ee593a9b6635206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102450607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a4611268228c1ec582b521138dcb3c845bdce7fa1381b22a39c255d5ff7e28`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cf553a1d689590ff4987101df413b6286a024eb13d9a13ad65e42a1999caff`  
		Last Modified: Tue, 14 Jan 2025 02:27:20 GMT  
		Size: 74.4 MB (74408514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df10519d0232bec08057b71fd3704f520f7da59f5e891731e021b62b3d10eb2e`  
		Last Modified: Tue, 14 Jan 2025 21:01:34 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:a56a1d194261b6e166f83e557e6e246e652542dd58c4544790a8c500318493b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d851a39eebad7d5543766ae04846fa07dcc4ce1df5329b3c6691a485681d7e`

```dockerfile
```

-	Layers:
	-	`sha256:194ab48a6e69122107093a054875cd870fd510d4847e6e8d47c373fc421bf232`  
		Last Modified: Tue, 14 Jan 2025 02:27:18 GMT  
		Size: 2.6 MB (2614762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc1f0ddfa38dd63521376d39ae56d217882859d1bf4716917e5524591bec9393`  
		Last Modified: Tue, 14 Jan 2025 02:27:17 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json
