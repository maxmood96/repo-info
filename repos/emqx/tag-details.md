<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.2`](#emqx52)
-	[`emqx:5.2.1`](#emqx521)
-	[`emqx:5.3`](#emqx53)
-	[`emqx:5.3.2`](#emqx532)
-	[`emqx:5.4`](#emqx54)
-	[`emqx:5.4.1`](#emqx541)
-	[`emqx:5.5`](#emqx55)
-	[`emqx:5.5.1`](#emqx551)
-	[`emqx:5.6`](#emqx56)
-	[`emqx:5.6.1`](#emqx561)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.2`](#emqx582)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:594a8c6809532d504d58407276ff01955addf60d3f59fae61e74134353ca44b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:9ba30d4c4f1b8b441b3bd717918ad3141d6c3fc4d887e3f67c526721606bd432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105938551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6b64a97a5267ba3c38fd16f53f01d98e30b907c0757bbe085ec81f47c2b924`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 13 Nov 2024 15:58:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 13 Nov 2024 15:58:01 GMT
ENV EMQX_VERSION=5.8.2
# Wed, 13 Nov 2024 15:58:01 GMT
ENV AMD64_SHA256=bd6497c8356a8d22b746788dc6b49d9447f370240724f6a32c96e9aaa82af7d7
# Wed, 13 Nov 2024 15:58:01 GMT
ENV ARM64_SHA256=18bd3d6a00ec243215faa4bb7a7bf4bf468b53384cc658b5e25ab55edd189551
# Wed, 13 Nov 2024 15:58:01 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 13 Nov 2024 15:58:01 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 13 Nov 2024 15:58:01 GMT
WORKDIR /opt/emqx
# Wed, 13 Nov 2024 15:58:01 GMT
USER emqx
# Wed, 13 Nov 2024 15:58:01 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 13 Nov 2024 15:58:01 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 13 Nov 2024 15:58:01 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 13 Nov 2024 15:58:01 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 13 Nov 2024 15:58:01 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2b943c0654cd96a70c907e4ebc3328059570101da14249a303b3bcf2a49d2f`  
		Last Modified: Tue, 03 Dec 2024 03:26:47 GMT  
		Size: 77.7 MB (77705908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10f3aeb1575b90475195ee2d459a18e49354863759adf26bb92ab9882361f2e`  
		Last Modified: Tue, 03 Dec 2024 03:26:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:6ce2645dd45c59a479f34cd4fe36bf277dde4c013ce5a82ce7afea9ea39391a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4b71f926055d7bf1def602b88364a619d010b70ef6cb1d63551ec06809a161`

```dockerfile
```

-	Layers:
	-	`sha256:c6888d18212025eb238adef1604b7da969a2a58c8a0af0d50802c0111462b7b8`  
		Last Modified: Tue, 03 Dec 2024 03:26:46 GMT  
		Size: 2.6 MB (2623511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:437f3cdc475f7d8974450ddf6b4ba678f7378e4e78dd5eea2f544c9943c631c1`  
		Last Modified: Tue, 03 Dec 2024 03:26:46 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a7d079b4c7b938a0ac551800495b751206ee84ddd2c67a5e374f1d31a348aecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (103030982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfc77a71346c452c6e5f73eac09ce51244abf9edfdb70e261a5c40f9e42d869`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 13 Nov 2024 15:58:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 13 Nov 2024 15:58:01 GMT
ENV EMQX_VERSION=5.8.2
# Wed, 13 Nov 2024 15:58:01 GMT
ENV AMD64_SHA256=bd6497c8356a8d22b746788dc6b49d9447f370240724f6a32c96e9aaa82af7d7
# Wed, 13 Nov 2024 15:58:01 GMT
ENV ARM64_SHA256=18bd3d6a00ec243215faa4bb7a7bf4bf468b53384cc658b5e25ab55edd189551
# Wed, 13 Nov 2024 15:58:01 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 13 Nov 2024 15:58:01 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 13 Nov 2024 15:58:01 GMT
WORKDIR /opt/emqx
# Wed, 13 Nov 2024 15:58:01 GMT
USER emqx
# Wed, 13 Nov 2024 15:58:01 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 13 Nov 2024 15:58:01 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 13 Nov 2024 15:58:01 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 13 Nov 2024 15:58:01 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 13 Nov 2024 15:58:01 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3e8fde570f1a3076d04645ce1f835d079c3fe965a78254b5d08dd63e6e50e4`  
		Last Modified: Tue, 03 Dec 2024 02:24:05 GMT  
		Size: 75.0 MB (74971110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12caf80a82dfec0188a966a0f4b2af135c159c389ff28cb8f5b39ba320b04a8e`  
		Last Modified: Tue, 03 Dec 2024 02:24:02 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:0ef6893ad5c614114ba0d8382d1173081c7a38dcea3342772133efa1b1375981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15841469471633e0ea9725d92675e0d7c3f5fa1b261adf9c851e9ea45e5cdc2`

```dockerfile
```

-	Layers:
	-	`sha256:ce3d48772c11a4468645d5d43f4479d4cc5b9c4c11416253ecd4342cc77443d2`  
		Last Modified: Tue, 03 Dec 2024 02:24:03 GMT  
		Size: 2.6 MB (2623790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a5367e11864430ec8fd8331a42f6885af2bb8cf4f6e95fda39dda76584ce2e3`  
		Last Modified: Tue, 03 Dec 2024 02:24:02 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.2`

```console
$ docker pull emqx@sha256:410bae37d53e56d09180eae3f67cfd1e476b0c25024f41e69e5e2965ee389145
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:d05089bae31e8407b12af47c5b1b013362cf7f2db7060d9eb36be9248aec7ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99575800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab37d02e8255fedd72a4281144e6df065c7f9f23e22e02d76af5e8e4738c4d7b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55883eec236593c18d4eba1dcf79b9850d75d5bb541675a384389758b3e5076`  
		Last Modified: Tue, 03 Dec 2024 02:14:15 GMT  
		Size: 1.4 MB (1424379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c250b7c7f8f04ff503f83027eeae08f8a49a956c49209231116bf11daf10b4`  
		Last Modified: Tue, 03 Dec 2024 02:14:14 GMT  
		Size: 4.0 KB (3991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f9a945470b972d8ab0d475f3726797b17c6b654e08964b405b78ac61436d35`  
		Last Modified: Tue, 03 Dec 2024 02:14:17 GMT  
		Size: 67.9 MB (67893854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04146b8f98c0d6c3ce522aabf03f877793475d7dfe78838a02f1bf3dce786562`  
		Last Modified: Tue, 03 Dec 2024 02:14:15 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2` - unknown; unknown

```console
$ docker pull emqx@sha256:2d5ba522946f28fad0396e43f88f8700fba23233467c4d40781d7339e1837540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45433d505335c7bbc2c4d851894a8431220f5ec67c5eaef723b8844ff5870df5`

```dockerfile
```

-	Layers:
	-	`sha256:0b2422cc729cc3e22371116e5c444dc405861bf342e41c6fd1da22cc57de9fc7`  
		Last Modified: Tue, 03 Dec 2024 02:14:15 GMT  
		Size: 2.8 MB (2829433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d4fa5e6fe9b4897a2f9083a87bc1caf3e22b529ba6cf1d89891f5882c80599`  
		Last Modified: Tue, 03 Dec 2024 02:14:14 GMT  
		Size: 15.8 KB (15842 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f587d7b14c396dc7fba48c71666e64ead8feb9eb689c338b12620dc6ef041c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89725702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b797e18cc22b7298040c31b2c4038a1e368e81cbf0b4f0f6a9fbad6204caef25`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597b6da494d39f8646e2d8000f4b86e0650f14c3a2f2910dabfabead3cdbfa5e`  
		Last Modified: Tue, 03 Dec 2024 02:20:39 GMT  
		Size: 1.4 MB (1438656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abae3e503f6376f72401dbfcc17282afae3e2e012807e9e07c4321dc3533e42`  
		Last Modified: Tue, 03 Dec 2024 02:20:39 GMT  
		Size: 4.0 KB (3996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c83bfbbd51c582252bafed6c6e1b1f48803316c78e2639737b03b0853600052`  
		Last Modified: Tue, 03 Dec 2024 02:20:41 GMT  
		Size: 59.5 MB (59537196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dcf0c0535a577f996c10c9654e92391ceecae3b79b2720f485a3463c6d3423`  
		Last Modified: Tue, 03 Dec 2024 02:20:39 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2` - unknown; unknown

```console
$ docker pull emqx@sha256:cbd603eeff03f1511bc8cf59c5fc7988d979b2d4df13350ed9fbc81094fc90e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a1aff3cbb7b200a403a229ce0e564bdc520265a687c56fe8edb847875f6c31`

```dockerfile
```

-	Layers:
	-	`sha256:8a090342f8e8ddda4be3aae3a60e27ace4bcf049da9e96e8d7f7f460d48ff035`  
		Last Modified: Tue, 03 Dec 2024 02:20:39 GMT  
		Size: 2.8 MB (2829668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:644fbbed5988422c269b0183f01c80276e560f99f15ea0b7c558d7c8190f9ea4`  
		Last Modified: Tue, 03 Dec 2024 02:20:39 GMT  
		Size: 15.9 KB (15950 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:410bae37d53e56d09180eae3f67cfd1e476b0c25024f41e69e5e2965ee389145
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:d05089bae31e8407b12af47c5b1b013362cf7f2db7060d9eb36be9248aec7ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99575800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab37d02e8255fedd72a4281144e6df065c7f9f23e22e02d76af5e8e4738c4d7b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55883eec236593c18d4eba1dcf79b9850d75d5bb541675a384389758b3e5076`  
		Last Modified: Tue, 03 Dec 2024 02:14:15 GMT  
		Size: 1.4 MB (1424379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c250b7c7f8f04ff503f83027eeae08f8a49a956c49209231116bf11daf10b4`  
		Last Modified: Tue, 03 Dec 2024 02:14:14 GMT  
		Size: 4.0 KB (3991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f9a945470b972d8ab0d475f3726797b17c6b654e08964b405b78ac61436d35`  
		Last Modified: Tue, 03 Dec 2024 02:14:17 GMT  
		Size: 67.9 MB (67893854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04146b8f98c0d6c3ce522aabf03f877793475d7dfe78838a02f1bf3dce786562`  
		Last Modified: Tue, 03 Dec 2024 02:14:15 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2.1` - unknown; unknown

```console
$ docker pull emqx@sha256:2d5ba522946f28fad0396e43f88f8700fba23233467c4d40781d7339e1837540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45433d505335c7bbc2c4d851894a8431220f5ec67c5eaef723b8844ff5870df5`

```dockerfile
```

-	Layers:
	-	`sha256:0b2422cc729cc3e22371116e5c444dc405861bf342e41c6fd1da22cc57de9fc7`  
		Last Modified: Tue, 03 Dec 2024 02:14:15 GMT  
		Size: 2.8 MB (2829433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d4fa5e6fe9b4897a2f9083a87bc1caf3e22b529ba6cf1d89891f5882c80599`  
		Last Modified: Tue, 03 Dec 2024 02:14:14 GMT  
		Size: 15.8 KB (15842 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.2.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f587d7b14c396dc7fba48c71666e64ead8feb9eb689c338b12620dc6ef041c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89725702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b797e18cc22b7298040c31b2c4038a1e368e81cbf0b4f0f6a9fbad6204caef25`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597b6da494d39f8646e2d8000f4b86e0650f14c3a2f2910dabfabead3cdbfa5e`  
		Last Modified: Tue, 03 Dec 2024 02:20:39 GMT  
		Size: 1.4 MB (1438656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abae3e503f6376f72401dbfcc17282afae3e2e012807e9e07c4321dc3533e42`  
		Last Modified: Tue, 03 Dec 2024 02:20:39 GMT  
		Size: 4.0 KB (3996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c83bfbbd51c582252bafed6c6e1b1f48803316c78e2639737b03b0853600052`  
		Last Modified: Tue, 03 Dec 2024 02:20:41 GMT  
		Size: 59.5 MB (59537196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dcf0c0535a577f996c10c9654e92391ceecae3b79b2720f485a3463c6d3423`  
		Last Modified: Tue, 03 Dec 2024 02:20:39 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2.1` - unknown; unknown

```console
$ docker pull emqx@sha256:cbd603eeff03f1511bc8cf59c5fc7988d979b2d4df13350ed9fbc81094fc90e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a1aff3cbb7b200a403a229ce0e564bdc520265a687c56fe8edb847875f6c31`

```dockerfile
```

-	Layers:
	-	`sha256:8a090342f8e8ddda4be3aae3a60e27ace4bcf049da9e96e8d7f7f460d48ff035`  
		Last Modified: Tue, 03 Dec 2024 02:20:39 GMT  
		Size: 2.8 MB (2829668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:644fbbed5988422c269b0183f01c80276e560f99f15ea0b7c558d7c8190f9ea4`  
		Last Modified: Tue, 03 Dec 2024 02:20:39 GMT  
		Size: 15.9 KB (15950 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.3`

```console
$ docker pull emqx@sha256:140e405b10cc8ebf026be5065ee50d73c9c3aa9423cf965d3125b1502227eab5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:69d264f1a9e15ccd41333c896c71a4279ea6670bfeaf32d1dc8b404664fff1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100409168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33e1ca9b99c51ce879d68b7073b82b578bec37cd60b76f2a98ab16e1d8f346f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf2b1abcc11a88f4c27ff29fcce01bd42666dd85d799174c853c270aa53fc67`  
		Last Modified: Tue, 03 Dec 2024 02:14:13 GMT  
		Size: 70.2 MB (70155593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6011dbe693e506da46596ebecfb73aec95a0140e72a3eb49b0139032801f25c`  
		Last Modified: Tue, 03 Dec 2024 02:14:11 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3` - unknown; unknown

```console
$ docker pull emqx@sha256:c8110d20c6cad7e8824e3b48a5a46199d2c932ea2c461cd61bccc1f4483c0d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2854619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388a5dc388cd91c5f713664f917c36a6282fa8230c8bb1e4d86752d5575a4006`

```dockerfile
```

-	Layers:
	-	`sha256:9563b9250c66cc5deeead5ddbc46ef4c0e77aa555ca7b6605a743686fd270320`  
		Last Modified: Tue, 03 Dec 2024 02:14:11 GMT  
		Size: 2.8 MB (2841836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f91c6dd84a805b90f320190b1f624719af52b59ae59112ec69d0ba19059dfc45`  
		Last Modified: Tue, 03 Dec 2024 02:14:11 GMT  
		Size: 12.8 KB (12783 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:9fb130d4b23f4cbcf884aaeebcc3c35842675733f75d83896fd1a93c82411ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90551169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd4cad9a1bb5aa0dae63b5a996ef7e7f1a2e92355bcd917573805f71e7978bc`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd44736819f761a54dd337659ad99a224e8bd6d89867e0b470a38c23ca9d907`  
		Last Modified: Tue, 03 Dec 2024 02:21:11 GMT  
		Size: 61.8 MB (61805314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88acb03e530a8df5bcbaf8a418fa9e3220b712874755281fae757d35720d1f3d`  
		Last Modified: Tue, 03 Dec 2024 02:21:09 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3` - unknown; unknown

```console
$ docker pull emqx@sha256:c20e7c0236b333c2c104844fc11cebf67847606deb9ba47519438a2f52e9eb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2854934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90baa14a0f42eb39e1355b8e5698dc6d7fff86501adb298409b364799a38c860`

```dockerfile
```

-	Layers:
	-	`sha256:ecc5609e6e46cfb7dcb3e665841d5d8dfa9261052b713923e7709d3c084263f7`  
		Last Modified: Tue, 03 Dec 2024 02:21:09 GMT  
		Size: 2.8 MB (2842071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:746663bbd0c2b164e28886adc61f22f09f08a7393da54b7f25e91fb1cd053a25`  
		Last Modified: Tue, 03 Dec 2024 02:21:09 GMT  
		Size: 12.9 KB (12863 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:140e405b10cc8ebf026be5065ee50d73c9c3aa9423cf965d3125b1502227eab5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:69d264f1a9e15ccd41333c896c71a4279ea6670bfeaf32d1dc8b404664fff1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100409168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33e1ca9b99c51ce879d68b7073b82b578bec37cd60b76f2a98ab16e1d8f346f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf2b1abcc11a88f4c27ff29fcce01bd42666dd85d799174c853c270aa53fc67`  
		Last Modified: Tue, 03 Dec 2024 02:14:13 GMT  
		Size: 70.2 MB (70155593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6011dbe693e506da46596ebecfb73aec95a0140e72a3eb49b0139032801f25c`  
		Last Modified: Tue, 03 Dec 2024 02:14:11 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3.2` - unknown; unknown

```console
$ docker pull emqx@sha256:c8110d20c6cad7e8824e3b48a5a46199d2c932ea2c461cd61bccc1f4483c0d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2854619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388a5dc388cd91c5f713664f917c36a6282fa8230c8bb1e4d86752d5575a4006`

```dockerfile
```

-	Layers:
	-	`sha256:9563b9250c66cc5deeead5ddbc46ef4c0e77aa555ca7b6605a743686fd270320`  
		Last Modified: Tue, 03 Dec 2024 02:14:11 GMT  
		Size: 2.8 MB (2841836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f91c6dd84a805b90f320190b1f624719af52b59ae59112ec69d0ba19059dfc45`  
		Last Modified: Tue, 03 Dec 2024 02:14:11 GMT  
		Size: 12.8 KB (12783 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.3.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:9fb130d4b23f4cbcf884aaeebcc3c35842675733f75d83896fd1a93c82411ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90551169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd4cad9a1bb5aa0dae63b5a996ef7e7f1a2e92355bcd917573805f71e7978bc`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd44736819f761a54dd337659ad99a224e8bd6d89867e0b470a38c23ca9d907`  
		Last Modified: Tue, 03 Dec 2024 02:21:11 GMT  
		Size: 61.8 MB (61805314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88acb03e530a8df5bcbaf8a418fa9e3220b712874755281fae757d35720d1f3d`  
		Last Modified: Tue, 03 Dec 2024 02:21:09 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3.2` - unknown; unknown

```console
$ docker pull emqx@sha256:c20e7c0236b333c2c104844fc11cebf67847606deb9ba47519438a2f52e9eb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2854934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90baa14a0f42eb39e1355b8e5698dc6d7fff86501adb298409b364799a38c860`

```dockerfile
```

-	Layers:
	-	`sha256:ecc5609e6e46cfb7dcb3e665841d5d8dfa9261052b713923e7709d3c084263f7`  
		Last Modified: Tue, 03 Dec 2024 02:21:09 GMT  
		Size: 2.8 MB (2842071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:746663bbd0c2b164e28886adc61f22f09f08a7393da54b7f25e91fb1cd053a25`  
		Last Modified: Tue, 03 Dec 2024 02:21:09 GMT  
		Size: 12.9 KB (12863 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.4`

```console
$ docker pull emqx@sha256:531c96f8baadba32795e3ed538162057172a984d6f28ac9562454086b97888b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.4` - linux; amd64

```console
$ docker pull emqx@sha256:a459d574cd0159b2a6e66bba850ded0926438de84d24e81d40d79465aaf87181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117322302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c060eec46982dae8749fb41cc6060e854c12d7f2a7fa642645244463bd7b02bf`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6729de094e58edaa2c34e944a92c22f9dc17824c020831d6274a9c7c4958c68`  
		Last Modified: Tue, 03 Dec 2024 02:14:02 GMT  
		Size: 87.1 MB (87068726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500e4149ac36d28455baf4cc120db0a6f5ae7d022989f5e4a9be59079087ca76`  
		Last Modified: Tue, 03 Dec 2024 02:14:01 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4` - unknown; unknown

```console
$ docker pull emqx@sha256:49d1cf5a57546cc2469d1b79893c6a439695669f93c9d755aba138ead5e1dea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2847251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419f08f5bb8e18d2713ff0c1027622b5af4ee62fe36b2c2192994ac1e28ae48d`

```dockerfile
```

-	Layers:
	-	`sha256:434058baecac101205bcc3501fb35053fd028c8156fecfa74181220c56fa56b0`  
		Last Modified: Tue, 03 Dec 2024 02:14:01 GMT  
		Size: 2.8 MB (2834525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:458b7a764488020dc93e1f9a3aef686296c3c5973d7d0beee232ac2957ecbf35`  
		Last Modified: Tue, 03 Dec 2024 02:14:01 GMT  
		Size: 12.7 KB (12726 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6b482aed4524e3671a4a3c1fc641d4be1ffd838615a8ed6b5aebb02cb1219572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 MB (106950385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c147232f74c881032b763c9bdaf3c1907942e32e8e95a1b0a28123dedc0fb3f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a273289ed77eea871cabb78495c42cfd7b3120674e4489a4e629d3650f46d956`  
		Last Modified: Tue, 03 Dec 2024 02:21:44 GMT  
		Size: 78.2 MB (78204530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be7ca03b28154251a43ac98c0432b8d96432eec3a50dc800b2746d9ad29a073`  
		Last Modified: Tue, 03 Dec 2024 02:21:42 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4` - unknown; unknown

```console
$ docker pull emqx@sha256:38d73bc4bfade538dbcf577343d36e944fe0c440e1ae875da28117ff46021399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2847567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fea106c0076b7cc7f74fbea453547a9f123997ef46080c77e008f817908c13`

```dockerfile
```

-	Layers:
	-	`sha256:b7f4d86b76c55f8dfbed31ca082aaf54f54add61c8ecd65d9ef1f9a509d53e51`  
		Last Modified: Tue, 03 Dec 2024 02:21:42 GMT  
		Size: 2.8 MB (2834760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e2ff9a8aa01bdf757c4cbcba2f449dedbf8117e870a019d501e784a8f11b899`  
		Last Modified: Tue, 03 Dec 2024 02:21:42 GMT  
		Size: 12.8 KB (12807 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.4.1`

```console
$ docker pull emqx@sha256:531c96f8baadba32795e3ed538162057172a984d6f28ac9562454086b97888b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.4.1` - linux; amd64

```console
$ docker pull emqx@sha256:a459d574cd0159b2a6e66bba850ded0926438de84d24e81d40d79465aaf87181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117322302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c060eec46982dae8749fb41cc6060e854c12d7f2a7fa642645244463bd7b02bf`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6729de094e58edaa2c34e944a92c22f9dc17824c020831d6274a9c7c4958c68`  
		Last Modified: Tue, 03 Dec 2024 02:14:02 GMT  
		Size: 87.1 MB (87068726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500e4149ac36d28455baf4cc120db0a6f5ae7d022989f5e4a9be59079087ca76`  
		Last Modified: Tue, 03 Dec 2024 02:14:01 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4.1` - unknown; unknown

```console
$ docker pull emqx@sha256:49d1cf5a57546cc2469d1b79893c6a439695669f93c9d755aba138ead5e1dea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2847251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419f08f5bb8e18d2713ff0c1027622b5af4ee62fe36b2c2192994ac1e28ae48d`

```dockerfile
```

-	Layers:
	-	`sha256:434058baecac101205bcc3501fb35053fd028c8156fecfa74181220c56fa56b0`  
		Last Modified: Tue, 03 Dec 2024 02:14:01 GMT  
		Size: 2.8 MB (2834525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:458b7a764488020dc93e1f9a3aef686296c3c5973d7d0beee232ac2957ecbf35`  
		Last Modified: Tue, 03 Dec 2024 02:14:01 GMT  
		Size: 12.7 KB (12726 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.4.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6b482aed4524e3671a4a3c1fc641d4be1ffd838615a8ed6b5aebb02cb1219572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 MB (106950385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c147232f74c881032b763c9bdaf3c1907942e32e8e95a1b0a28123dedc0fb3f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a273289ed77eea871cabb78495c42cfd7b3120674e4489a4e629d3650f46d956`  
		Last Modified: Tue, 03 Dec 2024 02:21:44 GMT  
		Size: 78.2 MB (78204530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be7ca03b28154251a43ac98c0432b8d96432eec3a50dc800b2746d9ad29a073`  
		Last Modified: Tue, 03 Dec 2024 02:21:42 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4.1` - unknown; unknown

```console
$ docker pull emqx@sha256:38d73bc4bfade538dbcf577343d36e944fe0c440e1ae875da28117ff46021399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2847567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fea106c0076b7cc7f74fbea453547a9f123997ef46080c77e008f817908c13`

```dockerfile
```

-	Layers:
	-	`sha256:b7f4d86b76c55f8dfbed31ca082aaf54f54add61c8ecd65d9ef1f9a509d53e51`  
		Last Modified: Tue, 03 Dec 2024 02:21:42 GMT  
		Size: 2.8 MB (2834760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e2ff9a8aa01bdf757c4cbcba2f449dedbf8117e870a019d501e784a8f11b899`  
		Last Modified: Tue, 03 Dec 2024 02:21:42 GMT  
		Size: 12.8 KB (12807 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.5`

```console
$ docker pull emqx@sha256:3b03a78e990e6e6b84715725c7b46dde0321a94199b123f0ef1d8f4e99e933a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.5` - linux; amd64

```console
$ docker pull emqx@sha256:75373eb630501dc65bb231a48eb873f1bac4bbdf72fee557aa9348019907b290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119888617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828c0e494471499ea76aea8c668e3880e17ebbe9db2d2fcbe940dccb88dfdb03`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e24f438a79030d4debb24ebccc984a9ef80f8d76101e1e2364a2fe149815b2c`  
		Last Modified: Tue, 03 Dec 2024 02:14:06 GMT  
		Size: 89.6 MB (89634910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b551ee0c0ba168236c4d333c50a38b08a13bb9eab171812b0f1622ba70f6ef`  
		Last Modified: Tue, 03 Dec 2024 02:14:04 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5` - unknown; unknown

```console
$ docker pull emqx@sha256:51178740b79ed5314d168228ef1a1e393777bb2f05120e59821047b4441edb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2847315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00738dd94f529d4f1d18c1a3be19463caafafaae92aa82c1e56ff49c8b97da91`

```dockerfile
```

-	Layers:
	-	`sha256:97dae494d1f0837d27b1f33e5723fb2a5762bd40325304328204ff5e9d7054e7`  
		Last Modified: Tue, 03 Dec 2024 02:14:04 GMT  
		Size: 2.8 MB (2834486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e8f7e54a311075b7938dffc8a3274acc825154443eee49c6830fa932854902`  
		Last Modified: Tue, 03 Dec 2024 02:14:04 GMT  
		Size: 12.8 KB (12829 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:92d5d27c4c4f0c01b294e0a59a4de44eafc78084362492b77193e646d2f9a622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115249146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ce72c51ace2ae2bc3e79413360eea5b2680723a1277fcb6f3c6bfb30c72547`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c6c34752ee0aebafdaa269fbe2e8517fcc796b214be3bf631c89a4295c46ae`  
		Last Modified: Tue, 03 Dec 2024 02:22:18 GMT  
		Size: 86.5 MB (86503158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2154775b1ac5490c85e73b40f44471e77994d7c39085c095aed5f5d566acbe3c`  
		Last Modified: Tue, 03 Dec 2024 02:22:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5` - unknown; unknown

```console
$ docker pull emqx@sha256:f46f82960573a519a321214b9687309415ad0c921ed01d8258943769cae4d125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2847629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c9ac513dec5da487606bfda985708810e06337da7ea792f4948fae5ffb81fa`

```dockerfile
```

-	Layers:
	-	`sha256:7ac7d91a157b1ff908e64d4b506ea60b37d5018a1fd7cdb674be139d2afc2325`  
		Last Modified: Tue, 03 Dec 2024 02:22:16 GMT  
		Size: 2.8 MB (2834721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbcc190b1e150250c02baa49f0d599a8520a45c3098fefd8edae74223ed7aa8b`  
		Last Modified: Tue, 03 Dec 2024 02:22:16 GMT  
		Size: 12.9 KB (12908 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.5.1`

```console
$ docker pull emqx@sha256:3b03a78e990e6e6b84715725c7b46dde0321a94199b123f0ef1d8f4e99e933a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.5.1` - linux; amd64

```console
$ docker pull emqx@sha256:75373eb630501dc65bb231a48eb873f1bac4bbdf72fee557aa9348019907b290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119888617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828c0e494471499ea76aea8c668e3880e17ebbe9db2d2fcbe940dccb88dfdb03`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e24f438a79030d4debb24ebccc984a9ef80f8d76101e1e2364a2fe149815b2c`  
		Last Modified: Tue, 03 Dec 2024 02:14:06 GMT  
		Size: 89.6 MB (89634910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b551ee0c0ba168236c4d333c50a38b08a13bb9eab171812b0f1622ba70f6ef`  
		Last Modified: Tue, 03 Dec 2024 02:14:04 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:51178740b79ed5314d168228ef1a1e393777bb2f05120e59821047b4441edb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2847315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00738dd94f529d4f1d18c1a3be19463caafafaae92aa82c1e56ff49c8b97da91`

```dockerfile
```

-	Layers:
	-	`sha256:97dae494d1f0837d27b1f33e5723fb2a5762bd40325304328204ff5e9d7054e7`  
		Last Modified: Tue, 03 Dec 2024 02:14:04 GMT  
		Size: 2.8 MB (2834486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e8f7e54a311075b7938dffc8a3274acc825154443eee49c6830fa932854902`  
		Last Modified: Tue, 03 Dec 2024 02:14:04 GMT  
		Size: 12.8 KB (12829 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:92d5d27c4c4f0c01b294e0a59a4de44eafc78084362492b77193e646d2f9a622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115249146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ce72c51ace2ae2bc3e79413360eea5b2680723a1277fcb6f3c6bfb30c72547`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c6c34752ee0aebafdaa269fbe2e8517fcc796b214be3bf631c89a4295c46ae`  
		Last Modified: Tue, 03 Dec 2024 02:22:18 GMT  
		Size: 86.5 MB (86503158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2154775b1ac5490c85e73b40f44471e77994d7c39085c095aed5f5d566acbe3c`  
		Last Modified: Tue, 03 Dec 2024 02:22:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:f46f82960573a519a321214b9687309415ad0c921ed01d8258943769cae4d125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2847629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c9ac513dec5da487606bfda985708810e06337da7ea792f4948fae5ffb81fa`

```dockerfile
```

-	Layers:
	-	`sha256:7ac7d91a157b1ff908e64d4b506ea60b37d5018a1fd7cdb674be139d2afc2325`  
		Last Modified: Tue, 03 Dec 2024 02:22:16 GMT  
		Size: 2.8 MB (2834721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbcc190b1e150250c02baa49f0d599a8520a45c3098fefd8edae74223ed7aa8b`  
		Last Modified: Tue, 03 Dec 2024 02:22:16 GMT  
		Size: 12.9 KB (12908 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.6`

```console
$ docker pull emqx@sha256:4cbb5792d0fd17e02f3003cda571aeca343d954f05215f8ab20a5a3b21603755
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.6` - linux; amd64

```console
$ docker pull emqx@sha256:06f2341d1bf4ec8350a37a029dc5f6590c2dc95f181bebf1493d0f8e3a727f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123093971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5ff702742d32ef92978cc8fe0122f1a127f136e7c006de0a807b0c7f7324b9`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df4958fc4c12745b67c6cb6f282b7653c8bea4dcf83270f6220ed92095cdb3b`  
		Last Modified: Tue, 03 Dec 2024 02:14:04 GMT  
		Size: 94.9 MB (94861327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539647b5863ddf2d468a1415bc1a8436afc9c508260ddde6a08bea72a415271f`  
		Last Modified: Tue, 03 Dec 2024 02:14:03 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6` - unknown; unknown

```console
$ docker pull emqx@sha256:eb5de69bc016d38e4a0381ee5de31a0ce64a421704df6ab97def853fea78bfc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ed1b7fbce8aca2df8630b19f2c9473f72e931b0002c004fb3c6b81c37ef933`

```dockerfile
```

-	Layers:
	-	`sha256:f1161a672cefafe23591baa9ce42e9f620563bc37fcfab6b7dd642f0cd61c5be`  
		Last Modified: Tue, 03 Dec 2024 02:14:03 GMT  
		Size: 2.6 MB (2616677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:691919cab9f6f73718bab98e72750afa27c629bd6f5d1f1c3e0744d04c6b573c`  
		Last Modified: Tue, 03 Dec 2024 02:14:03 GMT  
		Size: 11.9 KB (11950 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:1164b6a524981be6ee3ee07899b7830bff04e67e6edf3d148e9964afa54aa3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119487624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb3e9db8fddc02f0de9efa67de9f560ccca0d81c7cb68f89c33b5972bd8efad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fa03effb9c7e360339c4967255f3828e41656598477f7d0172b84e56d562ae`  
		Last Modified: Tue, 03 Dec 2024 02:22:53 GMT  
		Size: 91.4 MB (91427752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f877afc8b4bcb9fe930097f0ac628f6c66bf54807785c9caa6678f527c0f8bb8`  
		Last Modified: Tue, 03 Dec 2024 02:22:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6` - unknown; unknown

```console
$ docker pull emqx@sha256:1723c70b460f77070677b817973d2631a7c784004c9bff4799ff2fcb86b20997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea756d99930fddf50e6711a577d33a8e05f763c048d54ea4a8ea8d5881e8f833`

```dockerfile
```

-	Layers:
	-	`sha256:0f7647fd49b2751222f0821d3c29e91aa5ed9ebc4b79f125da99ac0593845c8c`  
		Last Modified: Tue, 03 Dec 2024 02:22:51 GMT  
		Size: 2.6 MB (2616932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3ab91b473515e70e296fc50237141d4e656bf230060757b0378a2255df306e1`  
		Last Modified: Tue, 03 Dec 2024 02:22:50 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.6.1`

```console
$ docker pull emqx@sha256:4cbb5792d0fd17e02f3003cda571aeca343d954f05215f8ab20a5a3b21603755
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.6.1` - linux; amd64

```console
$ docker pull emqx@sha256:06f2341d1bf4ec8350a37a029dc5f6590c2dc95f181bebf1493d0f8e3a727f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123093971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5ff702742d32ef92978cc8fe0122f1a127f136e7c006de0a807b0c7f7324b9`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df4958fc4c12745b67c6cb6f282b7653c8bea4dcf83270f6220ed92095cdb3b`  
		Last Modified: Tue, 03 Dec 2024 02:14:04 GMT  
		Size: 94.9 MB (94861327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539647b5863ddf2d468a1415bc1a8436afc9c508260ddde6a08bea72a415271f`  
		Last Modified: Tue, 03 Dec 2024 02:14:03 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6.1` - unknown; unknown

```console
$ docker pull emqx@sha256:eb5de69bc016d38e4a0381ee5de31a0ce64a421704df6ab97def853fea78bfc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ed1b7fbce8aca2df8630b19f2c9473f72e931b0002c004fb3c6b81c37ef933`

```dockerfile
```

-	Layers:
	-	`sha256:f1161a672cefafe23591baa9ce42e9f620563bc37fcfab6b7dd642f0cd61c5be`  
		Last Modified: Tue, 03 Dec 2024 02:14:03 GMT  
		Size: 2.6 MB (2616677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:691919cab9f6f73718bab98e72750afa27c629bd6f5d1f1c3e0744d04c6b573c`  
		Last Modified: Tue, 03 Dec 2024 02:14:03 GMT  
		Size: 11.9 KB (11950 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.6.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:1164b6a524981be6ee3ee07899b7830bff04e67e6edf3d148e9964afa54aa3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119487624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb3e9db8fddc02f0de9efa67de9f560ccca0d81c7cb68f89c33b5972bd8efad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fa03effb9c7e360339c4967255f3828e41656598477f7d0172b84e56d562ae`  
		Last Modified: Tue, 03 Dec 2024 02:22:53 GMT  
		Size: 91.4 MB (91427752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f877afc8b4bcb9fe930097f0ac628f6c66bf54807785c9caa6678f527c0f8bb8`  
		Last Modified: Tue, 03 Dec 2024 02:22:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6.1` - unknown; unknown

```console
$ docker pull emqx@sha256:1723c70b460f77070677b817973d2631a7c784004c9bff4799ff2fcb86b20997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea756d99930fddf50e6711a577d33a8e05f763c048d54ea4a8ea8d5881e8f833`

```dockerfile
```

-	Layers:
	-	`sha256:0f7647fd49b2751222f0821d3c29e91aa5ed9ebc4b79f125da99ac0593845c8c`  
		Last Modified: Tue, 03 Dec 2024 02:22:51 GMT  
		Size: 2.6 MB (2616932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3ab91b473515e70e296fc50237141d4e656bf230060757b0378a2255df306e1`  
		Last Modified: Tue, 03 Dec 2024 02:22:50 GMT  
		Size: 12.0 KB (12031 bytes)  
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
$ docker pull emqx@sha256:594a8c6809532d504d58407276ff01955addf60d3f59fae61e74134353ca44b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:9ba30d4c4f1b8b441b3bd717918ad3141d6c3fc4d887e3f67c526721606bd432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105938551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6b64a97a5267ba3c38fd16f53f01d98e30b907c0757bbe085ec81f47c2b924`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 13 Nov 2024 15:58:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 13 Nov 2024 15:58:01 GMT
ENV EMQX_VERSION=5.8.2
# Wed, 13 Nov 2024 15:58:01 GMT
ENV AMD64_SHA256=bd6497c8356a8d22b746788dc6b49d9447f370240724f6a32c96e9aaa82af7d7
# Wed, 13 Nov 2024 15:58:01 GMT
ENV ARM64_SHA256=18bd3d6a00ec243215faa4bb7a7bf4bf468b53384cc658b5e25ab55edd189551
# Wed, 13 Nov 2024 15:58:01 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 13 Nov 2024 15:58:01 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 13 Nov 2024 15:58:01 GMT
WORKDIR /opt/emqx
# Wed, 13 Nov 2024 15:58:01 GMT
USER emqx
# Wed, 13 Nov 2024 15:58:01 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 13 Nov 2024 15:58:01 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 13 Nov 2024 15:58:01 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 13 Nov 2024 15:58:01 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 13 Nov 2024 15:58:01 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2b943c0654cd96a70c907e4ebc3328059570101da14249a303b3bcf2a49d2f`  
		Last Modified: Tue, 03 Dec 2024 03:26:47 GMT  
		Size: 77.7 MB (77705908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10f3aeb1575b90475195ee2d459a18e49354863759adf26bb92ab9882361f2e`  
		Last Modified: Tue, 03 Dec 2024 03:26:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:6ce2645dd45c59a479f34cd4fe36bf277dde4c013ce5a82ce7afea9ea39391a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4b71f926055d7bf1def602b88364a619d010b70ef6cb1d63551ec06809a161`

```dockerfile
```

-	Layers:
	-	`sha256:c6888d18212025eb238adef1604b7da969a2a58c8a0af0d50802c0111462b7b8`  
		Last Modified: Tue, 03 Dec 2024 03:26:46 GMT  
		Size: 2.6 MB (2623511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:437f3cdc475f7d8974450ddf6b4ba678f7378e4e78dd5eea2f544c9943c631c1`  
		Last Modified: Tue, 03 Dec 2024 03:26:46 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a7d079b4c7b938a0ac551800495b751206ee84ddd2c67a5e374f1d31a348aecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (103030982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfc77a71346c452c6e5f73eac09ce51244abf9edfdb70e261a5c40f9e42d869`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 13 Nov 2024 15:58:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 13 Nov 2024 15:58:01 GMT
ENV EMQX_VERSION=5.8.2
# Wed, 13 Nov 2024 15:58:01 GMT
ENV AMD64_SHA256=bd6497c8356a8d22b746788dc6b49d9447f370240724f6a32c96e9aaa82af7d7
# Wed, 13 Nov 2024 15:58:01 GMT
ENV ARM64_SHA256=18bd3d6a00ec243215faa4bb7a7bf4bf468b53384cc658b5e25ab55edd189551
# Wed, 13 Nov 2024 15:58:01 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 13 Nov 2024 15:58:01 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 13 Nov 2024 15:58:01 GMT
WORKDIR /opt/emqx
# Wed, 13 Nov 2024 15:58:01 GMT
USER emqx
# Wed, 13 Nov 2024 15:58:01 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 13 Nov 2024 15:58:01 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 13 Nov 2024 15:58:01 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 13 Nov 2024 15:58:01 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 13 Nov 2024 15:58:01 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3e8fde570f1a3076d04645ce1f835d079c3fe965a78254b5d08dd63e6e50e4`  
		Last Modified: Tue, 03 Dec 2024 02:24:05 GMT  
		Size: 75.0 MB (74971110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12caf80a82dfec0188a966a0f4b2af135c159c389ff28cb8f5b39ba320b04a8e`  
		Last Modified: Tue, 03 Dec 2024 02:24:02 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:0ef6893ad5c614114ba0d8382d1173081c7a38dcea3342772133efa1b1375981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15841469471633e0ea9725d92675e0d7c3f5fa1b261adf9c851e9ea45e5cdc2`

```dockerfile
```

-	Layers:
	-	`sha256:ce3d48772c11a4468645d5d43f4479d4cc5b9c4c11416253ecd4342cc77443d2`  
		Last Modified: Tue, 03 Dec 2024 02:24:03 GMT  
		Size: 2.6 MB (2623790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a5367e11864430ec8fd8331a42f6885af2bb8cf4f6e95fda39dda76584ce2e3`  
		Last Modified: Tue, 03 Dec 2024 02:24:02 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.2`

```console
$ docker pull emqx@sha256:594a8c6809532d504d58407276ff01955addf60d3f59fae61e74134353ca44b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.2` - linux; amd64

```console
$ docker pull emqx@sha256:9ba30d4c4f1b8b441b3bd717918ad3141d6c3fc4d887e3f67c526721606bd432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105938551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6b64a97a5267ba3c38fd16f53f01d98e30b907c0757bbe085ec81f47c2b924`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 13 Nov 2024 15:58:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 13 Nov 2024 15:58:01 GMT
ENV EMQX_VERSION=5.8.2
# Wed, 13 Nov 2024 15:58:01 GMT
ENV AMD64_SHA256=bd6497c8356a8d22b746788dc6b49d9447f370240724f6a32c96e9aaa82af7d7
# Wed, 13 Nov 2024 15:58:01 GMT
ENV ARM64_SHA256=18bd3d6a00ec243215faa4bb7a7bf4bf468b53384cc658b5e25ab55edd189551
# Wed, 13 Nov 2024 15:58:01 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 13 Nov 2024 15:58:01 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 13 Nov 2024 15:58:01 GMT
WORKDIR /opt/emqx
# Wed, 13 Nov 2024 15:58:01 GMT
USER emqx
# Wed, 13 Nov 2024 15:58:01 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 13 Nov 2024 15:58:01 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 13 Nov 2024 15:58:01 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 13 Nov 2024 15:58:01 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 13 Nov 2024 15:58:01 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2b943c0654cd96a70c907e4ebc3328059570101da14249a303b3bcf2a49d2f`  
		Last Modified: Tue, 03 Dec 2024 03:26:47 GMT  
		Size: 77.7 MB (77705908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10f3aeb1575b90475195ee2d459a18e49354863759adf26bb92ab9882361f2e`  
		Last Modified: Tue, 03 Dec 2024 03:26:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.2` - unknown; unknown

```console
$ docker pull emqx@sha256:6ce2645dd45c59a479f34cd4fe36bf277dde4c013ce5a82ce7afea9ea39391a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4b71f926055d7bf1def602b88364a619d010b70ef6cb1d63551ec06809a161`

```dockerfile
```

-	Layers:
	-	`sha256:c6888d18212025eb238adef1604b7da969a2a58c8a0af0d50802c0111462b7b8`  
		Last Modified: Tue, 03 Dec 2024 03:26:46 GMT  
		Size: 2.6 MB (2623511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:437f3cdc475f7d8974450ddf6b4ba678f7378e4e78dd5eea2f544c9943c631c1`  
		Last Modified: Tue, 03 Dec 2024 03:26:46 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a7d079b4c7b938a0ac551800495b751206ee84ddd2c67a5e374f1d31a348aecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (103030982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfc77a71346c452c6e5f73eac09ce51244abf9edfdb70e261a5c40f9e42d869`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 13 Nov 2024 15:58:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 13 Nov 2024 15:58:01 GMT
ENV EMQX_VERSION=5.8.2
# Wed, 13 Nov 2024 15:58:01 GMT
ENV AMD64_SHA256=bd6497c8356a8d22b746788dc6b49d9447f370240724f6a32c96e9aaa82af7d7
# Wed, 13 Nov 2024 15:58:01 GMT
ENV ARM64_SHA256=18bd3d6a00ec243215faa4bb7a7bf4bf468b53384cc658b5e25ab55edd189551
# Wed, 13 Nov 2024 15:58:01 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 13 Nov 2024 15:58:01 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 13 Nov 2024 15:58:01 GMT
WORKDIR /opt/emqx
# Wed, 13 Nov 2024 15:58:01 GMT
USER emqx
# Wed, 13 Nov 2024 15:58:01 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 13 Nov 2024 15:58:01 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 13 Nov 2024 15:58:01 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 13 Nov 2024 15:58:01 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 13 Nov 2024 15:58:01 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3e8fde570f1a3076d04645ce1f835d079c3fe965a78254b5d08dd63e6e50e4`  
		Last Modified: Tue, 03 Dec 2024 02:24:05 GMT  
		Size: 75.0 MB (74971110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12caf80a82dfec0188a966a0f4b2af135c159c389ff28cb8f5b39ba320b04a8e`  
		Last Modified: Tue, 03 Dec 2024 02:24:02 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.2` - unknown; unknown

```console
$ docker pull emqx@sha256:0ef6893ad5c614114ba0d8382d1173081c7a38dcea3342772133efa1b1375981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15841469471633e0ea9725d92675e0d7c3f5fa1b261adf9c851e9ea45e5cdc2`

```dockerfile
```

-	Layers:
	-	`sha256:ce3d48772c11a4468645d5d43f4479d4cc5b9c4c11416253ecd4342cc77443d2`  
		Last Modified: Tue, 03 Dec 2024 02:24:03 GMT  
		Size: 2.6 MB (2623790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a5367e11864430ec8fd8331a42f6885af2bb8cf4f6e95fda39dda76584ce2e3`  
		Last Modified: Tue, 03 Dec 2024 02:24:02 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:594a8c6809532d504d58407276ff01955addf60d3f59fae61e74134353ca44b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:9ba30d4c4f1b8b441b3bd717918ad3141d6c3fc4d887e3f67c526721606bd432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105938551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6b64a97a5267ba3c38fd16f53f01d98e30b907c0757bbe085ec81f47c2b924`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 13 Nov 2024 15:58:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 13 Nov 2024 15:58:01 GMT
ENV EMQX_VERSION=5.8.2
# Wed, 13 Nov 2024 15:58:01 GMT
ENV AMD64_SHA256=bd6497c8356a8d22b746788dc6b49d9447f370240724f6a32c96e9aaa82af7d7
# Wed, 13 Nov 2024 15:58:01 GMT
ENV ARM64_SHA256=18bd3d6a00ec243215faa4bb7a7bf4bf468b53384cc658b5e25ab55edd189551
# Wed, 13 Nov 2024 15:58:01 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 13 Nov 2024 15:58:01 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 13 Nov 2024 15:58:01 GMT
WORKDIR /opt/emqx
# Wed, 13 Nov 2024 15:58:01 GMT
USER emqx
# Wed, 13 Nov 2024 15:58:01 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 13 Nov 2024 15:58:01 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 13 Nov 2024 15:58:01 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 13 Nov 2024 15:58:01 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 13 Nov 2024 15:58:01 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2b943c0654cd96a70c907e4ebc3328059570101da14249a303b3bcf2a49d2f`  
		Last Modified: Tue, 03 Dec 2024 03:26:47 GMT  
		Size: 77.7 MB (77705908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10f3aeb1575b90475195ee2d459a18e49354863759adf26bb92ab9882361f2e`  
		Last Modified: Tue, 03 Dec 2024 03:26:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:6ce2645dd45c59a479f34cd4fe36bf277dde4c013ce5a82ce7afea9ea39391a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4b71f926055d7bf1def602b88364a619d010b70ef6cb1d63551ec06809a161`

```dockerfile
```

-	Layers:
	-	`sha256:c6888d18212025eb238adef1604b7da969a2a58c8a0af0d50802c0111462b7b8`  
		Last Modified: Tue, 03 Dec 2024 03:26:46 GMT  
		Size: 2.6 MB (2623511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:437f3cdc475f7d8974450ddf6b4ba678f7378e4e78dd5eea2f544c9943c631c1`  
		Last Modified: Tue, 03 Dec 2024 03:26:46 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a7d079b4c7b938a0ac551800495b751206ee84ddd2c67a5e374f1d31a348aecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (103030982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfc77a71346c452c6e5f73eac09ce51244abf9edfdb70e261a5c40f9e42d869`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 13 Nov 2024 15:58:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 13 Nov 2024 15:58:01 GMT
ENV EMQX_VERSION=5.8.2
# Wed, 13 Nov 2024 15:58:01 GMT
ENV AMD64_SHA256=bd6497c8356a8d22b746788dc6b49d9447f370240724f6a32c96e9aaa82af7d7
# Wed, 13 Nov 2024 15:58:01 GMT
ENV ARM64_SHA256=18bd3d6a00ec243215faa4bb7a7bf4bf468b53384cc658b5e25ab55edd189551
# Wed, 13 Nov 2024 15:58:01 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 13 Nov 2024 15:58:01 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 13 Nov 2024 15:58:01 GMT
WORKDIR /opt/emqx
# Wed, 13 Nov 2024 15:58:01 GMT
USER emqx
# Wed, 13 Nov 2024 15:58:01 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 13 Nov 2024 15:58:01 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 13 Nov 2024 15:58:01 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 13 Nov 2024 15:58:01 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 13 Nov 2024 15:58:01 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3e8fde570f1a3076d04645ce1f835d079c3fe965a78254b5d08dd63e6e50e4`  
		Last Modified: Tue, 03 Dec 2024 02:24:05 GMT  
		Size: 75.0 MB (74971110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12caf80a82dfec0188a966a0f4b2af135c159c389ff28cb8f5b39ba320b04a8e`  
		Last Modified: Tue, 03 Dec 2024 02:24:02 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:0ef6893ad5c614114ba0d8382d1173081c7a38dcea3342772133efa1b1375981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15841469471633e0ea9725d92675e0d7c3f5fa1b261adf9c851e9ea45e5cdc2`

```dockerfile
```

-	Layers:
	-	`sha256:ce3d48772c11a4468645d5d43f4479d4cc5b9c4c11416253ecd4342cc77443d2`  
		Last Modified: Tue, 03 Dec 2024 02:24:03 GMT  
		Size: 2.6 MB (2623790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a5367e11864430ec8fd8331a42f6885af2bb8cf4f6e95fda39dda76584ce2e3`  
		Last Modified: Tue, 03 Dec 2024 02:24:02 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json
