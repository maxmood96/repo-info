<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.8`](#emqx588)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:b1ce4ec6fb2c52a730ff25a6fa1396737318d6d29cb621bb616503337518cd98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:209dc9c955533dac3ae57642a970949458ee7b364adc19e483882ef892a7c7cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108405596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f963165e86dd65d4b8ce5f08f5853001b6c98576daa89e86d27d950cb96e4a1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:20 GMT
ENV EMQX_VERSION=5.8.8
# Wed, 22 Apr 2026 01:15:20 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Wed, 22 Apr 2026 01:15:20 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Wed, 22 Apr 2026 01:15:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 22 Apr 2026 01:15:20 GMT
WORKDIR /opt/emqx
# Wed, 22 Apr 2026 01:15:20 GMT
USER emqx
# Wed, 22 Apr 2026 01:15:20 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 22 Apr 2026 01:15:20 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 22 Apr 2026 01:15:20 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 22 Apr 2026 01:15:20 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:15:20 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771242cc041a54b850741c2ff15408cc214aca4cc035d45e545538e44e62a781`  
		Last Modified: Wed, 22 Apr 2026 01:15:34 GMT  
		Size: 78.6 MB (78624360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffd18b91e68b74e488aa5c703a69d5cda6ca01779ec5a9725b5e45a00ccbdcc`  
		Last Modified: Wed, 22 Apr 2026 01:15:31 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:ce1901c066f137f52ec30dcb71b17dae397b08823bae867f5120cd245741e431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febe6df9ee37bb7de93b978b4a909f3cc59e5f9811a805e5bf9605c8eee2e505`

```dockerfile
```

-	Layers:
	-	`sha256:235b38402cb1e6f9512e3b993ba77467e9b304de439c4f3af00d00c7af0a7d61`  
		Last Modified: Wed, 22 Apr 2026 01:15:32 GMT  
		Size: 2.4 MB (2403501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b68b461a753bacb5f41f5dcf4db7e7041147f7d324198cdfb99a5584d8294ac0`  
		Last Modified: Wed, 22 Apr 2026 01:15:32 GMT  
		Size: 12.5 KB (12485 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:db2d0aaab3003bb12c5dfceeed0e4316f97fc2df2e361d80de40642660d58668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106676241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33245892fbd206f0bdbeaa01ec39b15aebbafc49a5daefb7462d0e4b96a93ad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:32 GMT
ENV EMQX_VERSION=5.8.8
# Wed, 22 Apr 2026 01:15:32 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Wed, 22 Apr 2026 01:15:32 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Wed, 22 Apr 2026 01:15:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 22 Apr 2026 01:15:32 GMT
WORKDIR /opt/emqx
# Wed, 22 Apr 2026 01:15:32 GMT
USER emqx
# Wed, 22 Apr 2026 01:15:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 22 Apr 2026 01:15:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 22 Apr 2026 01:15:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 22 Apr 2026 01:15:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:15:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a741c87dc1b859f3dd772a7e0cd203663139e885369e5255a2cb18871514778`  
		Last Modified: Wed, 22 Apr 2026 01:15:48 GMT  
		Size: 76.5 MB (76531572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a61c6ce5e744538b256fdf9091150ffb22fc9725e87b7655f6ac39f6a59f3a1`  
		Last Modified: Wed, 22 Apr 2026 01:15:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:4ea0142fbc2290b673a8748810885297b595d7573175cc329780baa682368e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55bd10dbea96a90aa5e3479a208653a490d7d9f2a61050f2029980e082295b2`

```dockerfile
```

-	Layers:
	-	`sha256:d524a693b67eacb9ff1e6f0549665f8cf5e792caa2f5fa429a6d38a4fc8381ab`  
		Last Modified: Wed, 22 Apr 2026 01:15:45 GMT  
		Size: 2.4 MB (2403790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5493bd5654dc2c43b436bad847e4dbf93c776ef71ad06ba4a3ddbe7e33b3163f`  
		Last Modified: Wed, 22 Apr 2026 01:15:45 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:875216f0215c704cca5b138d1eb3f16504a30ec7047f6fc4f7b57cc2413ab372
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:821a1cc61aad973fe22bb096332790e4c899d2ffee537010609eea67d79303be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125393777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f534df8a34a849ae7a6191350a30daf39a40e36123dec8e64beb17b7176ff5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:15:40 GMT
ENV EMQX_VERSION=5.7.2
# Wed, 22 Apr 2026 01:15:40 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Wed, 22 Apr 2026 01:15:40 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Wed, 22 Apr 2026 01:15:40 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 22 Apr 2026 01:15:40 GMT
WORKDIR /opt/emqx
# Wed, 22 Apr 2026 01:15:40 GMT
USER emqx
# Wed, 22 Apr 2026 01:15:40 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 22 Apr 2026 01:15:40 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 22 Apr 2026 01:15:40 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 22 Apr 2026 01:15:40 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:15:40 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79703699bc8b439f3b15a4aaacf1d0337dd25d8f11a577601e560855e286c462`  
		Last Modified: Wed, 22 Apr 2026 01:15:58 GMT  
		Size: 97.2 MB (97156462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d840d16c4a611411cb417b92e6f9a20514d2da8e12201bc636a980fe0d4bc78c`  
		Last Modified: Wed, 22 Apr 2026 01:15:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:a922e5153a46a4c25fe70934382a1c290c5c8ebf99f5d50185c0ed77dfc18e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8d6b515b230908ef84dd56d7f95c457ee4e0855513babf835f6d4d1071df6c`

```dockerfile
```

-	Layers:
	-	`sha256:8890c7dd927b603f210cc47a09638e6f52f341df803f40fd1e7f706adb01ffcc`  
		Last Modified: Wed, 22 Apr 2026 01:15:55 GMT  
		Size: 2.8 MB (2751398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72ecc5eafac96cbd6815e5b6f0b989ee2bac348cbe907123f0e85948cb1f199a`  
		Last Modified: Wed, 22 Apr 2026 01:15:56 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8334c347b5dd23f3d6223216bf21b9d03a1bf4222e7fcefde5f8eac65da925db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121835303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a158aeb359d58e4d247864715a8516deafdb3f482e07e3d7aafd2fe650fdcb`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:15:22 GMT
ENV EMQX_VERSION=5.7.2
# Wed, 22 Apr 2026 01:15:22 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Wed, 22 Apr 2026 01:15:22 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Wed, 22 Apr 2026 01:15:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 22 Apr 2026 01:15:22 GMT
WORKDIR /opt/emqx
# Wed, 22 Apr 2026 01:15:22 GMT
USER emqx
# Wed, 22 Apr 2026 01:15:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 22 Apr 2026 01:15:22 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 22 Apr 2026 01:15:22 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 22 Apr 2026 01:15:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:15:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feef95dddab53ec358edd5585c6a6a740193ea76878e2bc8bed29e7dc9bb62ff`  
		Last Modified: Wed, 22 Apr 2026 01:15:40 GMT  
		Size: 93.7 MB (93718126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec60d95aa305e9269af9846851187d9c1dc9c5fdd09d4cdd4e2582407d6ef1d`  
		Last Modified: Wed, 22 Apr 2026 01:15:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:5c4e6640b8ff3449ab60192647d1a1da3c6fb5d3cee31a7025f51e20c32dc1f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce48a21830c90c39a88319acf5c1b9ad0d86d5dd5debe70de4abc7f17f624068`

```dockerfile
```

-	Layers:
	-	`sha256:ad8b366bb98e6e23f1ea84d18d86296b4ad681100b13361839cf4ff811c566fe`  
		Last Modified: Wed, 22 Apr 2026 01:15:38 GMT  
		Size: 2.8 MB (2751654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27641f27cdf4e2b3f7e8674db4ba9b2f73810e7e43f4d70d56a55c94ece3bf44`  
		Last Modified: Wed, 22 Apr 2026 01:15:37 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:875216f0215c704cca5b138d1eb3f16504a30ec7047f6fc4f7b57cc2413ab372
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:821a1cc61aad973fe22bb096332790e4c899d2ffee537010609eea67d79303be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125393777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f534df8a34a849ae7a6191350a30daf39a40e36123dec8e64beb17b7176ff5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:15:40 GMT
ENV EMQX_VERSION=5.7.2
# Wed, 22 Apr 2026 01:15:40 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Wed, 22 Apr 2026 01:15:40 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Wed, 22 Apr 2026 01:15:40 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 22 Apr 2026 01:15:40 GMT
WORKDIR /opt/emqx
# Wed, 22 Apr 2026 01:15:40 GMT
USER emqx
# Wed, 22 Apr 2026 01:15:40 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 22 Apr 2026 01:15:40 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 22 Apr 2026 01:15:40 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 22 Apr 2026 01:15:40 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:15:40 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79703699bc8b439f3b15a4aaacf1d0337dd25d8f11a577601e560855e286c462`  
		Last Modified: Wed, 22 Apr 2026 01:15:58 GMT  
		Size: 97.2 MB (97156462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d840d16c4a611411cb417b92e6f9a20514d2da8e12201bc636a980fe0d4bc78c`  
		Last Modified: Wed, 22 Apr 2026 01:15:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:a922e5153a46a4c25fe70934382a1c290c5c8ebf99f5d50185c0ed77dfc18e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8d6b515b230908ef84dd56d7f95c457ee4e0855513babf835f6d4d1071df6c`

```dockerfile
```

-	Layers:
	-	`sha256:8890c7dd927b603f210cc47a09638e6f52f341df803f40fd1e7f706adb01ffcc`  
		Last Modified: Wed, 22 Apr 2026 01:15:55 GMT  
		Size: 2.8 MB (2751398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72ecc5eafac96cbd6815e5b6f0b989ee2bac348cbe907123f0e85948cb1f199a`  
		Last Modified: Wed, 22 Apr 2026 01:15:56 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8334c347b5dd23f3d6223216bf21b9d03a1bf4222e7fcefde5f8eac65da925db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121835303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a158aeb359d58e4d247864715a8516deafdb3f482e07e3d7aafd2fe650fdcb`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:15:22 GMT
ENV EMQX_VERSION=5.7.2
# Wed, 22 Apr 2026 01:15:22 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Wed, 22 Apr 2026 01:15:22 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Wed, 22 Apr 2026 01:15:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 22 Apr 2026 01:15:22 GMT
WORKDIR /opt/emqx
# Wed, 22 Apr 2026 01:15:22 GMT
USER emqx
# Wed, 22 Apr 2026 01:15:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 22 Apr 2026 01:15:22 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 22 Apr 2026 01:15:22 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 22 Apr 2026 01:15:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:15:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feef95dddab53ec358edd5585c6a6a740193ea76878e2bc8bed29e7dc9bb62ff`  
		Last Modified: Wed, 22 Apr 2026 01:15:40 GMT  
		Size: 93.7 MB (93718126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec60d95aa305e9269af9846851187d9c1dc9c5fdd09d4cdd4e2582407d6ef1d`  
		Last Modified: Wed, 22 Apr 2026 01:15:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:5c4e6640b8ff3449ab60192647d1a1da3c6fb5d3cee31a7025f51e20c32dc1f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce48a21830c90c39a88319acf5c1b9ad0d86d5dd5debe70de4abc7f17f624068`

```dockerfile
```

-	Layers:
	-	`sha256:ad8b366bb98e6e23f1ea84d18d86296b4ad681100b13361839cf4ff811c566fe`  
		Last Modified: Wed, 22 Apr 2026 01:15:38 GMT  
		Size: 2.8 MB (2751654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27641f27cdf4e2b3f7e8674db4ba9b2f73810e7e43f4d70d56a55c94ece3bf44`  
		Last Modified: Wed, 22 Apr 2026 01:15:37 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:b1ce4ec6fb2c52a730ff25a6fa1396737318d6d29cb621bb616503337518cd98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:209dc9c955533dac3ae57642a970949458ee7b364adc19e483882ef892a7c7cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108405596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f963165e86dd65d4b8ce5f08f5853001b6c98576daa89e86d27d950cb96e4a1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:20 GMT
ENV EMQX_VERSION=5.8.8
# Wed, 22 Apr 2026 01:15:20 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Wed, 22 Apr 2026 01:15:20 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Wed, 22 Apr 2026 01:15:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 22 Apr 2026 01:15:20 GMT
WORKDIR /opt/emqx
# Wed, 22 Apr 2026 01:15:20 GMT
USER emqx
# Wed, 22 Apr 2026 01:15:20 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 22 Apr 2026 01:15:20 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 22 Apr 2026 01:15:20 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 22 Apr 2026 01:15:20 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:15:20 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771242cc041a54b850741c2ff15408cc214aca4cc035d45e545538e44e62a781`  
		Last Modified: Wed, 22 Apr 2026 01:15:34 GMT  
		Size: 78.6 MB (78624360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffd18b91e68b74e488aa5c703a69d5cda6ca01779ec5a9725b5e45a00ccbdcc`  
		Last Modified: Wed, 22 Apr 2026 01:15:31 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:ce1901c066f137f52ec30dcb71b17dae397b08823bae867f5120cd245741e431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febe6df9ee37bb7de93b978b4a909f3cc59e5f9811a805e5bf9605c8eee2e505`

```dockerfile
```

-	Layers:
	-	`sha256:235b38402cb1e6f9512e3b993ba77467e9b304de439c4f3af00d00c7af0a7d61`  
		Last Modified: Wed, 22 Apr 2026 01:15:32 GMT  
		Size: 2.4 MB (2403501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b68b461a753bacb5f41f5dcf4db7e7041147f7d324198cdfb99a5584d8294ac0`  
		Last Modified: Wed, 22 Apr 2026 01:15:32 GMT  
		Size: 12.5 KB (12485 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:db2d0aaab3003bb12c5dfceeed0e4316f97fc2df2e361d80de40642660d58668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106676241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33245892fbd206f0bdbeaa01ec39b15aebbafc49a5daefb7462d0e4b96a93ad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:32 GMT
ENV EMQX_VERSION=5.8.8
# Wed, 22 Apr 2026 01:15:32 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Wed, 22 Apr 2026 01:15:32 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Wed, 22 Apr 2026 01:15:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 22 Apr 2026 01:15:32 GMT
WORKDIR /opt/emqx
# Wed, 22 Apr 2026 01:15:32 GMT
USER emqx
# Wed, 22 Apr 2026 01:15:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 22 Apr 2026 01:15:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 22 Apr 2026 01:15:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 22 Apr 2026 01:15:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:15:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a741c87dc1b859f3dd772a7e0cd203663139e885369e5255a2cb18871514778`  
		Last Modified: Wed, 22 Apr 2026 01:15:48 GMT  
		Size: 76.5 MB (76531572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a61c6ce5e744538b256fdf9091150ffb22fc9725e87b7655f6ac39f6a59f3a1`  
		Last Modified: Wed, 22 Apr 2026 01:15:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:4ea0142fbc2290b673a8748810885297b595d7573175cc329780baa682368e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55bd10dbea96a90aa5e3479a208653a490d7d9f2a61050f2029980e082295b2`

```dockerfile
```

-	Layers:
	-	`sha256:d524a693b67eacb9ff1e6f0549665f8cf5e792caa2f5fa429a6d38a4fc8381ab`  
		Last Modified: Wed, 22 Apr 2026 01:15:45 GMT  
		Size: 2.4 MB (2403790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5493bd5654dc2c43b436bad847e4dbf93c776ef71ad06ba4a3ddbe7e33b3163f`  
		Last Modified: Wed, 22 Apr 2026 01:15:45 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.8`

```console
$ docker pull emqx@sha256:b1ce4ec6fb2c52a730ff25a6fa1396737318d6d29cb621bb616503337518cd98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.8` - linux; amd64

```console
$ docker pull emqx@sha256:209dc9c955533dac3ae57642a970949458ee7b364adc19e483882ef892a7c7cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108405596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f963165e86dd65d4b8ce5f08f5853001b6c98576daa89e86d27d950cb96e4a1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:20 GMT
ENV EMQX_VERSION=5.8.8
# Wed, 22 Apr 2026 01:15:20 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Wed, 22 Apr 2026 01:15:20 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Wed, 22 Apr 2026 01:15:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 22 Apr 2026 01:15:20 GMT
WORKDIR /opt/emqx
# Wed, 22 Apr 2026 01:15:20 GMT
USER emqx
# Wed, 22 Apr 2026 01:15:20 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 22 Apr 2026 01:15:20 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 22 Apr 2026 01:15:20 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 22 Apr 2026 01:15:20 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:15:20 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771242cc041a54b850741c2ff15408cc214aca4cc035d45e545538e44e62a781`  
		Last Modified: Wed, 22 Apr 2026 01:15:34 GMT  
		Size: 78.6 MB (78624360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffd18b91e68b74e488aa5c703a69d5cda6ca01779ec5a9725b5e45a00ccbdcc`  
		Last Modified: Wed, 22 Apr 2026 01:15:31 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:ce1901c066f137f52ec30dcb71b17dae397b08823bae867f5120cd245741e431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febe6df9ee37bb7de93b978b4a909f3cc59e5f9811a805e5bf9605c8eee2e505`

```dockerfile
```

-	Layers:
	-	`sha256:235b38402cb1e6f9512e3b993ba77467e9b304de439c4f3af00d00c7af0a7d61`  
		Last Modified: Wed, 22 Apr 2026 01:15:32 GMT  
		Size: 2.4 MB (2403501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b68b461a753bacb5f41f5dcf4db7e7041147f7d324198cdfb99a5584d8294ac0`  
		Last Modified: Wed, 22 Apr 2026 01:15:32 GMT  
		Size: 12.5 KB (12485 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:db2d0aaab3003bb12c5dfceeed0e4316f97fc2df2e361d80de40642660d58668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106676241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33245892fbd206f0bdbeaa01ec39b15aebbafc49a5daefb7462d0e4b96a93ad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:32 GMT
ENV EMQX_VERSION=5.8.8
# Wed, 22 Apr 2026 01:15:32 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Wed, 22 Apr 2026 01:15:32 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Wed, 22 Apr 2026 01:15:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 22 Apr 2026 01:15:32 GMT
WORKDIR /opt/emqx
# Wed, 22 Apr 2026 01:15:32 GMT
USER emqx
# Wed, 22 Apr 2026 01:15:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 22 Apr 2026 01:15:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 22 Apr 2026 01:15:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 22 Apr 2026 01:15:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:15:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a741c87dc1b859f3dd772a7e0cd203663139e885369e5255a2cb18871514778`  
		Last Modified: Wed, 22 Apr 2026 01:15:48 GMT  
		Size: 76.5 MB (76531572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a61c6ce5e744538b256fdf9091150ffb22fc9725e87b7655f6ac39f6a59f3a1`  
		Last Modified: Wed, 22 Apr 2026 01:15:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:4ea0142fbc2290b673a8748810885297b595d7573175cc329780baa682368e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55bd10dbea96a90aa5e3479a208653a490d7d9f2a61050f2029980e082295b2`

```dockerfile
```

-	Layers:
	-	`sha256:d524a693b67eacb9ff1e6f0549665f8cf5e792caa2f5fa429a6d38a4fc8381ab`  
		Last Modified: Wed, 22 Apr 2026 01:15:45 GMT  
		Size: 2.4 MB (2403790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5493bd5654dc2c43b436bad847e4dbf93c776ef71ad06ba4a3ddbe7e33b3163f`  
		Last Modified: Wed, 22 Apr 2026 01:15:45 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:b1ce4ec6fb2c52a730ff25a6fa1396737318d6d29cb621bb616503337518cd98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:209dc9c955533dac3ae57642a970949458ee7b364adc19e483882ef892a7c7cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108405596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f963165e86dd65d4b8ce5f08f5853001b6c98576daa89e86d27d950cb96e4a1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:20 GMT
ENV EMQX_VERSION=5.8.8
# Wed, 22 Apr 2026 01:15:20 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Wed, 22 Apr 2026 01:15:20 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Wed, 22 Apr 2026 01:15:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 22 Apr 2026 01:15:20 GMT
WORKDIR /opt/emqx
# Wed, 22 Apr 2026 01:15:20 GMT
USER emqx
# Wed, 22 Apr 2026 01:15:20 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 22 Apr 2026 01:15:20 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 22 Apr 2026 01:15:20 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 22 Apr 2026 01:15:20 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:15:20 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771242cc041a54b850741c2ff15408cc214aca4cc035d45e545538e44e62a781`  
		Last Modified: Wed, 22 Apr 2026 01:15:34 GMT  
		Size: 78.6 MB (78624360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffd18b91e68b74e488aa5c703a69d5cda6ca01779ec5a9725b5e45a00ccbdcc`  
		Last Modified: Wed, 22 Apr 2026 01:15:31 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:ce1901c066f137f52ec30dcb71b17dae397b08823bae867f5120cd245741e431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febe6df9ee37bb7de93b978b4a909f3cc59e5f9811a805e5bf9605c8eee2e505`

```dockerfile
```

-	Layers:
	-	`sha256:235b38402cb1e6f9512e3b993ba77467e9b304de439c4f3af00d00c7af0a7d61`  
		Last Modified: Wed, 22 Apr 2026 01:15:32 GMT  
		Size: 2.4 MB (2403501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b68b461a753bacb5f41f5dcf4db7e7041147f7d324198cdfb99a5584d8294ac0`  
		Last Modified: Wed, 22 Apr 2026 01:15:32 GMT  
		Size: 12.5 KB (12485 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:db2d0aaab3003bb12c5dfceeed0e4316f97fc2df2e361d80de40642660d58668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106676241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33245892fbd206f0bdbeaa01ec39b15aebbafc49a5daefb7462d0e4b96a93ad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:32 GMT
ENV EMQX_VERSION=5.8.8
# Wed, 22 Apr 2026 01:15:32 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Wed, 22 Apr 2026 01:15:32 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Wed, 22 Apr 2026 01:15:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 22 Apr 2026 01:15:32 GMT
WORKDIR /opt/emqx
# Wed, 22 Apr 2026 01:15:32 GMT
USER emqx
# Wed, 22 Apr 2026 01:15:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 22 Apr 2026 01:15:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 22 Apr 2026 01:15:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 22 Apr 2026 01:15:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:15:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a741c87dc1b859f3dd772a7e0cd203663139e885369e5255a2cb18871514778`  
		Last Modified: Wed, 22 Apr 2026 01:15:48 GMT  
		Size: 76.5 MB (76531572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a61c6ce5e744538b256fdf9091150ffb22fc9725e87b7655f6ac39f6a59f3a1`  
		Last Modified: Wed, 22 Apr 2026 01:15:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:4ea0142fbc2290b673a8748810885297b595d7573175cc329780baa682368e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55bd10dbea96a90aa5e3479a208653a490d7d9f2a61050f2029980e082295b2`

```dockerfile
```

-	Layers:
	-	`sha256:d524a693b67eacb9ff1e6f0549665f8cf5e792caa2f5fa429a6d38a4fc8381ab`  
		Last Modified: Wed, 22 Apr 2026 01:15:45 GMT  
		Size: 2.4 MB (2403790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5493bd5654dc2c43b436bad847e4dbf93c776ef71ad06ba4a3ddbe7e33b3163f`  
		Last Modified: Wed, 22 Apr 2026 01:15:45 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json
