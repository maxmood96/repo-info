<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.3`](#emqx583)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:33325e82da1b004a38f149d61afae67f64ba84dbaabe238fcb0aca3f25ae2e39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:96c3b09c7cba095720ccfd70d004f3a229d607d11d0091ba391d928d82514a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104930064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b20ac3087402d9fa55201ea2d6ca1fe2570cef8fc9acabd1a1fd92f27b05bd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Fri, 06 Dec 2024 08:46:43 GMT
ENV EMQX_VERSION=5.8.3
# Fri, 06 Dec 2024 08:46:43 GMT
ENV AMD64_SHA256=3342bf92b8e50ff44d001e3ddeaf5f14c447a2eb42cd1750c378f92195d6e963
# Fri, 06 Dec 2024 08:46:43 GMT
ENV ARM64_SHA256=a2f08ae1c79236485f66a1dca01cdf9b437d27aca0a75a9d37cff5a193f43737
# Fri, 06 Dec 2024 08:46:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 06 Dec 2024 08:46:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Fri, 06 Dec 2024 08:46:43 GMT
WORKDIR /opt/emqx
# Fri, 06 Dec 2024 08:46:43 GMT
USER emqx
# Fri, 06 Dec 2024 08:46:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 06 Dec 2024 08:46:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 06 Dec 2024 08:46:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 06 Dec 2024 08:46:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 06 Dec 2024 08:46:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a942a8fbd8e177c2ff308572a42a758d4322d84d47f220c8f1b4439fbc436389`  
		Last Modified: Fri, 06 Dec 2024 22:28:30 GMT  
		Size: 76.7 MB (76697418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b955257423ba70c1315a071c872b2b21f1543986e1fc3ec4f3f5a73b619b72fd`  
		Last Modified: Fri, 06 Dec 2024 22:28:29 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:508b1907e01436fa176287a086cbd1f4718ce3a8c27cd7943bfc1c58763f7ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ca240c0e34d51ac5c96e0d2b054b84d863ab0bf197b629b2070fbcc840a8fa`

```dockerfile
```

-	Layers:
	-	`sha256:fc94c4b7d7a0a6d943337e3c1b526dbd397818d9f85f109c93fc1e750ce2fec3`  
		Last Modified: Fri, 06 Dec 2024 22:28:29 GMT  
		Size: 2.6 MB (2615849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4cd6cf49e4af9418d2647cf1cd800532584dca21400a4cb893ef2b1b5003529`  
		Last Modified: Fri, 06 Dec 2024 22:28:29 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:73f00607f7031eb7328c7f6b721913256dcdc8c6d1d36af911378ecba73c8492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102031261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d08968d086a0c88f343a1cdfe294f5009d4492923fc399936fde235707ca9cb`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Fri, 06 Dec 2024 08:46:43 GMT
ENV EMQX_VERSION=5.8.3
# Fri, 06 Dec 2024 08:46:43 GMT
ENV AMD64_SHA256=3342bf92b8e50ff44d001e3ddeaf5f14c447a2eb42cd1750c378f92195d6e963
# Fri, 06 Dec 2024 08:46:43 GMT
ENV ARM64_SHA256=a2f08ae1c79236485f66a1dca01cdf9b437d27aca0a75a9d37cff5a193f43737
# Fri, 06 Dec 2024 08:46:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 06 Dec 2024 08:46:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Fri, 06 Dec 2024 08:46:43 GMT
WORKDIR /opt/emqx
# Fri, 06 Dec 2024 08:46:43 GMT
USER emqx
# Fri, 06 Dec 2024 08:46:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 06 Dec 2024 08:46:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 06 Dec 2024 08:46:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 06 Dec 2024 08:46:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 06 Dec 2024 08:46:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a8e40dca2f76e60bbf05e5b6e6130f6444c13cb80f2580bf58846fc57f7cd`  
		Last Modified: Fri, 06 Dec 2024 22:28:46 GMT  
		Size: 74.0 MB (73971386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f745e0834d67e81bf0b0d611d88038765ee48500dbc99163239d6d9496ec2b35`  
		Last Modified: Fri, 06 Dec 2024 22:28:43 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:162c7d337b107865db70b9b4bb1604bde846aaf2f8d96252c13b4e6568031f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a361a4a457e6913569f742eef76b0a33bcdb52df3f60a0e02d9310b411d25b8c`

```dockerfile
```

-	Layers:
	-	`sha256:d9c3a16926047ea4283fd48820e8d794a8ac49dc6face5d8e751d4b8a300893a`  
		Last Modified: Fri, 06 Dec 2024 22:28:44 GMT  
		Size: 2.6 MB (2616128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea0141f65dcee0bcef2a6a91282293a3edf80a5e3792a8754ff6ca9a824f6a5d`  
		Last Modified: Fri, 06 Dec 2024 22:28:43 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:ff3e01d67dae5eaa3df8ecb53919bae165b82057792029a9abbd9e599fdbd5ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:dd11f9b0537fb8f5c4b7f663af1c6798aa38cc7eb32ca016370f5c5c7f295e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125187627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e87c5d15edb56116e2358c99f9970a46f6846c91dc749dd99b20f5e78a6c146`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf4bc2fb86d146a0d2c0f15d1a94531f77cebe67e6612ca69f7d97899ac39ab`  
		Last Modified: Tue, 03 Dec 2024 03:26:50 GMT  
		Size: 97.0 MB (96954984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac1475541a3af7a73a6c779c93a999111333e295b86eb278887a77d9bd15fc3`  
		Last Modified: Tue, 03 Dec 2024 03:26:49 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:cf95886e061a2d36f7f29198a2103d6584923a72b81706e4c7a2e21b165775ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5810215e7cf3c9a9e26f31172e3d0810e547e9d373cff7ca82e37a5ca93806ea`

```dockerfile
```

-	Layers:
	-	`sha256:57f13fb65b1347b03a5d1563a58c1a896f1d0a408d7c747090a0b23fa8a220d3`  
		Last Modified: Tue, 03 Dec 2024 03:26:49 GMT  
		Size: 2.6 MB (2625173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0418351553cad17375b9a94eac91c14667a3d4cfbddd8b4671f6f8358bac9771`  
		Last Modified: Tue, 03 Dec 2024 03:26:49 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:dbd57520324a43b6d3c8ade816492990834227d8f3b90ded1b844143dd72a8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121561587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91b8d98164c4aa06da3f31ab23350b92cb6e74c75c488d3a55aefa4d2919c87`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d63daa7fa47836746e7fc05c550d26fd617fd0cee8400b355592e7a7a0c3ed0`  
		Last Modified: Tue, 03 Dec 2024 02:23:34 GMT  
		Size: 93.5 MB (93501714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d775fea4f391285ca45e259f5d0a0bfd840220bb483860536f72ea777cdcc48`  
		Last Modified: Tue, 03 Dec 2024 02:23:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:dabd6a5943050487152baa4b7c847b6cf78b45b4574c0cef4534e243ef73f3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d53439983a87ed3225f8773f2d049da9ad99e232b397ba2289df8de7eca43cb`

```dockerfile
```

-	Layers:
	-	`sha256:dd9e9a429ad4222061c1a052a94d2bbfa33c5dc85a68888e4e2a3a3ece3ea25f`  
		Last Modified: Tue, 03 Dec 2024 02:23:32 GMT  
		Size: 2.6 MB (2625428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9036fa8f45667ebf001bc3050b630d72472da7e5181aece44ba9177e51e3eaf1`  
		Last Modified: Tue, 03 Dec 2024 02:23:32 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:ff3e01d67dae5eaa3df8ecb53919bae165b82057792029a9abbd9e599fdbd5ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:dd11f9b0537fb8f5c4b7f663af1c6798aa38cc7eb32ca016370f5c5c7f295e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125187627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e87c5d15edb56116e2358c99f9970a46f6846c91dc749dd99b20f5e78a6c146`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf4bc2fb86d146a0d2c0f15d1a94531f77cebe67e6612ca69f7d97899ac39ab`  
		Last Modified: Tue, 03 Dec 2024 03:26:50 GMT  
		Size: 97.0 MB (96954984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac1475541a3af7a73a6c779c93a999111333e295b86eb278887a77d9bd15fc3`  
		Last Modified: Tue, 03 Dec 2024 03:26:49 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:cf95886e061a2d36f7f29198a2103d6584923a72b81706e4c7a2e21b165775ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5810215e7cf3c9a9e26f31172e3d0810e547e9d373cff7ca82e37a5ca93806ea`

```dockerfile
```

-	Layers:
	-	`sha256:57f13fb65b1347b03a5d1563a58c1a896f1d0a408d7c747090a0b23fa8a220d3`  
		Last Modified: Tue, 03 Dec 2024 03:26:49 GMT  
		Size: 2.6 MB (2625173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0418351553cad17375b9a94eac91c14667a3d4cfbddd8b4671f6f8358bac9771`  
		Last Modified: Tue, 03 Dec 2024 03:26:49 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:dbd57520324a43b6d3c8ade816492990834227d8f3b90ded1b844143dd72a8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121561587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91b8d98164c4aa06da3f31ab23350b92cb6e74c75c488d3a55aefa4d2919c87`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d63daa7fa47836746e7fc05c550d26fd617fd0cee8400b355592e7a7a0c3ed0`  
		Last Modified: Tue, 03 Dec 2024 02:23:34 GMT  
		Size: 93.5 MB (93501714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d775fea4f391285ca45e259f5d0a0bfd840220bb483860536f72ea777cdcc48`  
		Last Modified: Tue, 03 Dec 2024 02:23:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:dabd6a5943050487152baa4b7c847b6cf78b45b4574c0cef4534e243ef73f3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d53439983a87ed3225f8773f2d049da9ad99e232b397ba2289df8de7eca43cb`

```dockerfile
```

-	Layers:
	-	`sha256:dd9e9a429ad4222061c1a052a94d2bbfa33c5dc85a68888e4e2a3a3ece3ea25f`  
		Last Modified: Tue, 03 Dec 2024 02:23:32 GMT  
		Size: 2.6 MB (2625428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9036fa8f45667ebf001bc3050b630d72472da7e5181aece44ba9177e51e3eaf1`  
		Last Modified: Tue, 03 Dec 2024 02:23:32 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:33325e82da1b004a38f149d61afae67f64ba84dbaabe238fcb0aca3f25ae2e39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:96c3b09c7cba095720ccfd70d004f3a229d607d11d0091ba391d928d82514a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104930064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b20ac3087402d9fa55201ea2d6ca1fe2570cef8fc9acabd1a1fd92f27b05bd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Fri, 06 Dec 2024 08:46:43 GMT
ENV EMQX_VERSION=5.8.3
# Fri, 06 Dec 2024 08:46:43 GMT
ENV AMD64_SHA256=3342bf92b8e50ff44d001e3ddeaf5f14c447a2eb42cd1750c378f92195d6e963
# Fri, 06 Dec 2024 08:46:43 GMT
ENV ARM64_SHA256=a2f08ae1c79236485f66a1dca01cdf9b437d27aca0a75a9d37cff5a193f43737
# Fri, 06 Dec 2024 08:46:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 06 Dec 2024 08:46:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Fri, 06 Dec 2024 08:46:43 GMT
WORKDIR /opt/emqx
# Fri, 06 Dec 2024 08:46:43 GMT
USER emqx
# Fri, 06 Dec 2024 08:46:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 06 Dec 2024 08:46:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 06 Dec 2024 08:46:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 06 Dec 2024 08:46:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 06 Dec 2024 08:46:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a942a8fbd8e177c2ff308572a42a758d4322d84d47f220c8f1b4439fbc436389`  
		Last Modified: Fri, 06 Dec 2024 22:28:30 GMT  
		Size: 76.7 MB (76697418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b955257423ba70c1315a071c872b2b21f1543986e1fc3ec4f3f5a73b619b72fd`  
		Last Modified: Fri, 06 Dec 2024 22:28:29 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:508b1907e01436fa176287a086cbd1f4718ce3a8c27cd7943bfc1c58763f7ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ca240c0e34d51ac5c96e0d2b054b84d863ab0bf197b629b2070fbcc840a8fa`

```dockerfile
```

-	Layers:
	-	`sha256:fc94c4b7d7a0a6d943337e3c1b526dbd397818d9f85f109c93fc1e750ce2fec3`  
		Last Modified: Fri, 06 Dec 2024 22:28:29 GMT  
		Size: 2.6 MB (2615849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4cd6cf49e4af9418d2647cf1cd800532584dca21400a4cb893ef2b1b5003529`  
		Last Modified: Fri, 06 Dec 2024 22:28:29 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:73f00607f7031eb7328c7f6b721913256dcdc8c6d1d36af911378ecba73c8492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102031261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d08968d086a0c88f343a1cdfe294f5009d4492923fc399936fde235707ca9cb`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Fri, 06 Dec 2024 08:46:43 GMT
ENV EMQX_VERSION=5.8.3
# Fri, 06 Dec 2024 08:46:43 GMT
ENV AMD64_SHA256=3342bf92b8e50ff44d001e3ddeaf5f14c447a2eb42cd1750c378f92195d6e963
# Fri, 06 Dec 2024 08:46:43 GMT
ENV ARM64_SHA256=a2f08ae1c79236485f66a1dca01cdf9b437d27aca0a75a9d37cff5a193f43737
# Fri, 06 Dec 2024 08:46:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 06 Dec 2024 08:46:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Fri, 06 Dec 2024 08:46:43 GMT
WORKDIR /opt/emqx
# Fri, 06 Dec 2024 08:46:43 GMT
USER emqx
# Fri, 06 Dec 2024 08:46:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 06 Dec 2024 08:46:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 06 Dec 2024 08:46:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 06 Dec 2024 08:46:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 06 Dec 2024 08:46:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a8e40dca2f76e60bbf05e5b6e6130f6444c13cb80f2580bf58846fc57f7cd`  
		Last Modified: Fri, 06 Dec 2024 22:28:46 GMT  
		Size: 74.0 MB (73971386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f745e0834d67e81bf0b0d611d88038765ee48500dbc99163239d6d9496ec2b35`  
		Last Modified: Fri, 06 Dec 2024 22:28:43 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:162c7d337b107865db70b9b4bb1604bde846aaf2f8d96252c13b4e6568031f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a361a4a457e6913569f742eef76b0a33bcdb52df3f60a0e02d9310b411d25b8c`

```dockerfile
```

-	Layers:
	-	`sha256:d9c3a16926047ea4283fd48820e8d794a8ac49dc6face5d8e751d4b8a300893a`  
		Last Modified: Fri, 06 Dec 2024 22:28:44 GMT  
		Size: 2.6 MB (2616128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea0141f65dcee0bcef2a6a91282293a3edf80a5e3792a8754ff6ca9a824f6a5d`  
		Last Modified: Fri, 06 Dec 2024 22:28:43 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.3`

```console
$ docker pull emqx@sha256:33325e82da1b004a38f149d61afae67f64ba84dbaabe238fcb0aca3f25ae2e39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.3` - linux; amd64

```console
$ docker pull emqx@sha256:96c3b09c7cba095720ccfd70d004f3a229d607d11d0091ba391d928d82514a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104930064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b20ac3087402d9fa55201ea2d6ca1fe2570cef8fc9acabd1a1fd92f27b05bd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Fri, 06 Dec 2024 08:46:43 GMT
ENV EMQX_VERSION=5.8.3
# Fri, 06 Dec 2024 08:46:43 GMT
ENV AMD64_SHA256=3342bf92b8e50ff44d001e3ddeaf5f14c447a2eb42cd1750c378f92195d6e963
# Fri, 06 Dec 2024 08:46:43 GMT
ENV ARM64_SHA256=a2f08ae1c79236485f66a1dca01cdf9b437d27aca0a75a9d37cff5a193f43737
# Fri, 06 Dec 2024 08:46:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 06 Dec 2024 08:46:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Fri, 06 Dec 2024 08:46:43 GMT
WORKDIR /opt/emqx
# Fri, 06 Dec 2024 08:46:43 GMT
USER emqx
# Fri, 06 Dec 2024 08:46:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 06 Dec 2024 08:46:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 06 Dec 2024 08:46:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 06 Dec 2024 08:46:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 06 Dec 2024 08:46:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a942a8fbd8e177c2ff308572a42a758d4322d84d47f220c8f1b4439fbc436389`  
		Last Modified: Fri, 06 Dec 2024 22:28:30 GMT  
		Size: 76.7 MB (76697418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b955257423ba70c1315a071c872b2b21f1543986e1fc3ec4f3f5a73b619b72fd`  
		Last Modified: Fri, 06 Dec 2024 22:28:29 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.3` - unknown; unknown

```console
$ docker pull emqx@sha256:508b1907e01436fa176287a086cbd1f4718ce3a8c27cd7943bfc1c58763f7ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ca240c0e34d51ac5c96e0d2b054b84d863ab0bf197b629b2070fbcc840a8fa`

```dockerfile
```

-	Layers:
	-	`sha256:fc94c4b7d7a0a6d943337e3c1b526dbd397818d9f85f109c93fc1e750ce2fec3`  
		Last Modified: Fri, 06 Dec 2024 22:28:29 GMT  
		Size: 2.6 MB (2615849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4cd6cf49e4af9418d2647cf1cd800532584dca21400a4cb893ef2b1b5003529`  
		Last Modified: Fri, 06 Dec 2024 22:28:29 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:73f00607f7031eb7328c7f6b721913256dcdc8c6d1d36af911378ecba73c8492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102031261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d08968d086a0c88f343a1cdfe294f5009d4492923fc399936fde235707ca9cb`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Fri, 06 Dec 2024 08:46:43 GMT
ENV EMQX_VERSION=5.8.3
# Fri, 06 Dec 2024 08:46:43 GMT
ENV AMD64_SHA256=3342bf92b8e50ff44d001e3ddeaf5f14c447a2eb42cd1750c378f92195d6e963
# Fri, 06 Dec 2024 08:46:43 GMT
ENV ARM64_SHA256=a2f08ae1c79236485f66a1dca01cdf9b437d27aca0a75a9d37cff5a193f43737
# Fri, 06 Dec 2024 08:46:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 06 Dec 2024 08:46:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Fri, 06 Dec 2024 08:46:43 GMT
WORKDIR /opt/emqx
# Fri, 06 Dec 2024 08:46:43 GMT
USER emqx
# Fri, 06 Dec 2024 08:46:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 06 Dec 2024 08:46:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 06 Dec 2024 08:46:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 06 Dec 2024 08:46:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 06 Dec 2024 08:46:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a8e40dca2f76e60bbf05e5b6e6130f6444c13cb80f2580bf58846fc57f7cd`  
		Last Modified: Fri, 06 Dec 2024 22:28:46 GMT  
		Size: 74.0 MB (73971386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f745e0834d67e81bf0b0d611d88038765ee48500dbc99163239d6d9496ec2b35`  
		Last Modified: Fri, 06 Dec 2024 22:28:43 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.3` - unknown; unknown

```console
$ docker pull emqx@sha256:162c7d337b107865db70b9b4bb1604bde846aaf2f8d96252c13b4e6568031f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a361a4a457e6913569f742eef76b0a33bcdb52df3f60a0e02d9310b411d25b8c`

```dockerfile
```

-	Layers:
	-	`sha256:d9c3a16926047ea4283fd48820e8d794a8ac49dc6face5d8e751d4b8a300893a`  
		Last Modified: Fri, 06 Dec 2024 22:28:44 GMT  
		Size: 2.6 MB (2616128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea0141f65dcee0bcef2a6a91282293a3edf80a5e3792a8754ff6ca9a824f6a5d`  
		Last Modified: Fri, 06 Dec 2024 22:28:43 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:33325e82da1b004a38f149d61afae67f64ba84dbaabe238fcb0aca3f25ae2e39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:96c3b09c7cba095720ccfd70d004f3a229d607d11d0091ba391d928d82514a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104930064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b20ac3087402d9fa55201ea2d6ca1fe2570cef8fc9acabd1a1fd92f27b05bd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Fri, 06 Dec 2024 08:46:43 GMT
ENV EMQX_VERSION=5.8.3
# Fri, 06 Dec 2024 08:46:43 GMT
ENV AMD64_SHA256=3342bf92b8e50ff44d001e3ddeaf5f14c447a2eb42cd1750c378f92195d6e963
# Fri, 06 Dec 2024 08:46:43 GMT
ENV ARM64_SHA256=a2f08ae1c79236485f66a1dca01cdf9b437d27aca0a75a9d37cff5a193f43737
# Fri, 06 Dec 2024 08:46:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 06 Dec 2024 08:46:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Fri, 06 Dec 2024 08:46:43 GMT
WORKDIR /opt/emqx
# Fri, 06 Dec 2024 08:46:43 GMT
USER emqx
# Fri, 06 Dec 2024 08:46:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 06 Dec 2024 08:46:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 06 Dec 2024 08:46:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 06 Dec 2024 08:46:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 06 Dec 2024 08:46:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a942a8fbd8e177c2ff308572a42a758d4322d84d47f220c8f1b4439fbc436389`  
		Last Modified: Fri, 06 Dec 2024 22:28:30 GMT  
		Size: 76.7 MB (76697418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b955257423ba70c1315a071c872b2b21f1543986e1fc3ec4f3f5a73b619b72fd`  
		Last Modified: Fri, 06 Dec 2024 22:28:29 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:508b1907e01436fa176287a086cbd1f4718ce3a8c27cd7943bfc1c58763f7ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ca240c0e34d51ac5c96e0d2b054b84d863ab0bf197b629b2070fbcc840a8fa`

```dockerfile
```

-	Layers:
	-	`sha256:fc94c4b7d7a0a6d943337e3c1b526dbd397818d9f85f109c93fc1e750ce2fec3`  
		Last Modified: Fri, 06 Dec 2024 22:28:29 GMT  
		Size: 2.6 MB (2615849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4cd6cf49e4af9418d2647cf1cd800532584dca21400a4cb893ef2b1b5003529`  
		Last Modified: Fri, 06 Dec 2024 22:28:29 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:73f00607f7031eb7328c7f6b721913256dcdc8c6d1d36af911378ecba73c8492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102031261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d08968d086a0c88f343a1cdfe294f5009d4492923fc399936fde235707ca9cb`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Fri, 06 Dec 2024 08:46:43 GMT
ENV EMQX_VERSION=5.8.3
# Fri, 06 Dec 2024 08:46:43 GMT
ENV AMD64_SHA256=3342bf92b8e50ff44d001e3ddeaf5f14c447a2eb42cd1750c378f92195d6e963
# Fri, 06 Dec 2024 08:46:43 GMT
ENV ARM64_SHA256=a2f08ae1c79236485f66a1dca01cdf9b437d27aca0a75a9d37cff5a193f43737
# Fri, 06 Dec 2024 08:46:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 06 Dec 2024 08:46:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Fri, 06 Dec 2024 08:46:43 GMT
WORKDIR /opt/emqx
# Fri, 06 Dec 2024 08:46:43 GMT
USER emqx
# Fri, 06 Dec 2024 08:46:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 06 Dec 2024 08:46:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 06 Dec 2024 08:46:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 06 Dec 2024 08:46:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 06 Dec 2024 08:46:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a8e40dca2f76e60bbf05e5b6e6130f6444c13cb80f2580bf58846fc57f7cd`  
		Last Modified: Fri, 06 Dec 2024 22:28:46 GMT  
		Size: 74.0 MB (73971386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f745e0834d67e81bf0b0d611d88038765ee48500dbc99163239d6d9496ec2b35`  
		Last Modified: Fri, 06 Dec 2024 22:28:43 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:162c7d337b107865db70b9b4bb1604bde846aaf2f8d96252c13b4e6568031f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a361a4a457e6913569f742eef76b0a33bcdb52df3f60a0e02d9310b411d25b8c`

```dockerfile
```

-	Layers:
	-	`sha256:d9c3a16926047ea4283fd48820e8d794a8ac49dc6face5d8e751d4b8a300893a`  
		Last Modified: Fri, 06 Dec 2024 22:28:44 GMT  
		Size: 2.6 MB (2616128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea0141f65dcee0bcef2a6a91282293a3edf80a5e3792a8754ff6ca9a824f6a5d`  
		Last Modified: Fri, 06 Dec 2024 22:28:43 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json
