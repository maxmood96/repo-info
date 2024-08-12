<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.1`](#emqx51)
-	[`emqx:5.1.6`](#emqx516)
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
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:49ac9b12a15b7e649ceb25bd74d4c7a98209ffb9b1f58da6caa1b984e6a7fa99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:66c1f31561788effe34d9804299758d4927b7e11d8467297de202a96835f925f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126238122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fdc5370bf923bab8c90743b24666bca939fd1f2874c786e47d23fa1fbbfd87b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ea6242b71c16ce1352fcf57a0d11687c2bd0b9fd496834fd62f76dd8f5ebf2`  
		Last Modified: Tue, 23 Jul 2024 07:19:54 GMT  
		Size: 97.1 MB (97110772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312a74d0107a3ee33685af3838ac090917b45e87cb3006fc6192781d92482b4c`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:8e4ad0134f93a3a02b2167fa3392b9b80c19466227b895ce27358ee2077c37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f34cd44ade291f177d0677daa06c10214702867382053ae2ca28173d626e3f8`

```dockerfile
```

-	Layers:
	-	`sha256:7c83086fd6007886c99a90d7d357091c7e561d320beb2faba0c8bbcc497c6298`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 2.6 MB (2599757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4740c9a8c3c0fdbc38c099b4759c70dc685a1bdf61a78e9702f2e6540074d6fb`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:42fa6f5d51dd4ba31bb04c74579f94fb5b542d77f5c343e9c3228bd402e08a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122815516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d420029c6f6de2a2cba1437cbc6c2f0d54ad2b6d9b6f8d3b660bcd5e238f532d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3e2f4ab829a4ca9b003191cf0f7790b7f8a4ba88d1280ba1684b699b851a0f`  
		Last Modified: Tue, 23 Jul 2024 14:04:27 GMT  
		Size: 93.7 MB (93657881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7625bfd2ba9540151b7b03e0b66859a72db79e36e53e00ab542042e1239151`  
		Last Modified: Tue, 23 Jul 2024 14:04:25 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:c6a2b798d31866b3c57031fcc0f821d0d35f020673432ae507f1d3c3dfcd4334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03008f242bed4c64734934401a004fa899a10db53a69d1981ad7d1b24aa96d5`

```dockerfile
```

-	Layers:
	-	`sha256:16d279b421c442fa999b969231f6f8aab5a32a6e8b2e9ff61d0e93303a2ad438`  
		Last Modified: Tue, 23 Jul 2024 14:04:27 GMT  
		Size: 2.6 MB (2600036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62bbf9793a6fc5236d608a0a2aaf60339a8304868e0553b4269ca7e3da7f387f`  
		Last Modified: Tue, 23 Jul 2024 14:04:25 GMT  
		Size: 12.6 KB (12608 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.1`

```console
$ docker pull emqx@sha256:65b18f2999790cd234ed0d364e926c16480a34e6cd19889daaec85893809b895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:dbd0ac96beea6a7b58282e863f6d4387911d4afdcfe0acb61fe88a5c7fe7f6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102401399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c4b47dc0cf4028485ba4b3282946b530f6b17c3ebd6da0a20836f84e5b23b2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c29eb70beca3a9d65a22162f8772e56435d546ff0276c086630e4c28ed0567e`  
		Last Modified: Tue, 23 Jul 2024 07:19:21 GMT  
		Size: 3.0 MB (2987574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab66c95b99483ae60045e516ec652067ea908c43d5b0d5ecfd38439fb8968fe7`  
		Last Modified: Tue, 23 Jul 2024 07:19:21 GMT  
		Size: 4.0 KB (3987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a35cf555d7da20558a61409d839a9703de7a44df4826b7b7d7c2f1bb642ac`  
		Last Modified: Tue, 23 Jul 2024 07:19:23 GMT  
		Size: 68.0 MB (67980576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb005464fd444dafd24404013e16d680b6837ce0101f39aee07987b4cd3b1556`  
		Last Modified: Tue, 23 Jul 2024 07:19:21 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:09007f288dacdde2c458dda7643dfb04fb76f62bd41eed24bf790801e549f182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2876794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffb95c9945f66313d3e51d217bab2058e20e1227d04af334ce8d867bb9a94b0`

```dockerfile
```

-	Layers:
	-	`sha256:148d4052ae97cc5a36434cec0ab64b3b43fb8824c3cca687f7755ecb0ac2ea20`  
		Last Modified: Tue, 23 Jul 2024 07:19:21 GMT  
		Size: 2.9 MB (2861668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0109e7f9d0e071578e49ad062bb7dab1793c7abf98094079eb6998ffb3931a11`  
		Last Modified: Tue, 23 Jul 2024 07:19:20 GMT  
		Size: 15.1 KB (15126 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8c13f8628f71068bb0d43aaa77f54fa21f92da14c2bac084ac4456fa788cb0c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92705162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a353392ec907d607d780de60ee9a9eb546eabd3ce792c1fedbf17f73a2a8a416`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33fc2116065e6353fa8aa86f1c7507868be2cd2ee8bf489296524c2855c902c`  
		Last Modified: Tue, 23 Jul 2024 14:00:17 GMT  
		Size: 3.0 MB (3003821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f6e784c0c9d5fadcacd8e656264c1194d8be71e800337e013d33866dec0f06`  
		Last Modified: Tue, 23 Jul 2024 14:00:16 GMT  
		Size: 4.0 KB (3990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0a513d3851f2ac5e1ed1c0623dea386ba7e1b61869a170bf7f7e570328162b`  
		Last Modified: Tue, 23 Jul 2024 14:00:18 GMT  
		Size: 59.6 MB (59620336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad163ade3c59a5c3fb34725bd53fcbd9cd6ec4dfba8c855e1dda6e3185616ab`  
		Last Modified: Tue, 23 Jul 2024 14:00:16 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:b482eb12c7f3d5a73907eaee8ab55e235d38dcc1cbc5b9f31397feb103f5c16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11334b5302c075e4dacbf72647794a052bc15cfc77b84db5563fee9e4a0584b0`

```dockerfile
```

-	Layers:
	-	`sha256:22e601d6656aa8088a2542882419e4c4d4ffcb75c286f763044a00540ce5f5f7`  
		Last Modified: Tue, 23 Jul 2024 14:00:16 GMT  
		Size: 2.9 MB (2861915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e08a37acb9d3b0bf91d0f216f7e746c64e7db8b3ac3a9db9333dc008b8b6070`  
		Last Modified: Tue, 23 Jul 2024 14:00:16 GMT  
		Size: 15.4 KB (15407 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:65b18f2999790cd234ed0d364e926c16480a34e6cd19889daaec85893809b895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:dbd0ac96beea6a7b58282e863f6d4387911d4afdcfe0acb61fe88a5c7fe7f6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102401399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c4b47dc0cf4028485ba4b3282946b530f6b17c3ebd6da0a20836f84e5b23b2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c29eb70beca3a9d65a22162f8772e56435d546ff0276c086630e4c28ed0567e`  
		Last Modified: Tue, 23 Jul 2024 07:19:21 GMT  
		Size: 3.0 MB (2987574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab66c95b99483ae60045e516ec652067ea908c43d5b0d5ecfd38439fb8968fe7`  
		Last Modified: Tue, 23 Jul 2024 07:19:21 GMT  
		Size: 4.0 KB (3987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a35cf555d7da20558a61409d839a9703de7a44df4826b7b7d7c2f1bb642ac`  
		Last Modified: Tue, 23 Jul 2024 07:19:23 GMT  
		Size: 68.0 MB (67980576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb005464fd444dafd24404013e16d680b6837ce0101f39aee07987b4cd3b1556`  
		Last Modified: Tue, 23 Jul 2024 07:19:21 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1.6` - unknown; unknown

```console
$ docker pull emqx@sha256:09007f288dacdde2c458dda7643dfb04fb76f62bd41eed24bf790801e549f182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2876794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffb95c9945f66313d3e51d217bab2058e20e1227d04af334ce8d867bb9a94b0`

```dockerfile
```

-	Layers:
	-	`sha256:148d4052ae97cc5a36434cec0ab64b3b43fb8824c3cca687f7755ecb0ac2ea20`  
		Last Modified: Tue, 23 Jul 2024 07:19:21 GMT  
		Size: 2.9 MB (2861668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0109e7f9d0e071578e49ad062bb7dab1793c7abf98094079eb6998ffb3931a11`  
		Last Modified: Tue, 23 Jul 2024 07:19:20 GMT  
		Size: 15.1 KB (15126 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.1.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8c13f8628f71068bb0d43aaa77f54fa21f92da14c2bac084ac4456fa788cb0c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92705162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a353392ec907d607d780de60ee9a9eb546eabd3ce792c1fedbf17f73a2a8a416`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33fc2116065e6353fa8aa86f1c7507868be2cd2ee8bf489296524c2855c902c`  
		Last Modified: Tue, 23 Jul 2024 14:00:17 GMT  
		Size: 3.0 MB (3003821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f6e784c0c9d5fadcacd8e656264c1194d8be71e800337e013d33866dec0f06`  
		Last Modified: Tue, 23 Jul 2024 14:00:16 GMT  
		Size: 4.0 KB (3990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0a513d3851f2ac5e1ed1c0623dea386ba7e1b61869a170bf7f7e570328162b`  
		Last Modified: Tue, 23 Jul 2024 14:00:18 GMT  
		Size: 59.6 MB (59620336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad163ade3c59a5c3fb34725bd53fcbd9cd6ec4dfba8c855e1dda6e3185616ab`  
		Last Modified: Tue, 23 Jul 2024 14:00:16 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1.6` - unknown; unknown

```console
$ docker pull emqx@sha256:b482eb12c7f3d5a73907eaee8ab55e235d38dcc1cbc5b9f31397feb103f5c16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11334b5302c075e4dacbf72647794a052bc15cfc77b84db5563fee9e4a0584b0`

```dockerfile
```

-	Layers:
	-	`sha256:22e601d6656aa8088a2542882419e4c4d4ffcb75c286f763044a00540ce5f5f7`  
		Last Modified: Tue, 23 Jul 2024 14:00:16 GMT  
		Size: 2.9 MB (2861915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e08a37acb9d3b0bf91d0f216f7e746c64e7db8b3ac3a9db9333dc008b8b6070`  
		Last Modified: Tue, 23 Jul 2024 14:00:16 GMT  
		Size: 15.4 KB (15407 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.2`

```console
$ docker pull emqx@sha256:8841fd92e6398e9ebf8d048d1944ae404ef0b062e0526706045e9e28f65d387e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:a0849341eebb70b49fee29b693f9f123565dc4691a06de9e044459e467389e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (100956082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7a55867b2cd375ce93ac98c4df13776b6e900607d423711ebd61cf58188e64`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e189bca6085d98f7f8cbed0ab1b2102a4d2aac5a5e572323ccefc7fbe5ecdd3`  
		Last Modified: Tue, 23 Jul 2024 07:19:39 GMT  
		Size: 1.6 MB (1629027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba433d75d4bd1f3423515cbba9d3255248e2c6341dda4b1d9c38d0f22e9d822c`  
		Last Modified: Tue, 23 Jul 2024 07:19:38 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf15f68a2f2cd2e73ad2aea4fd6c47b28de391809b83cec9471e70a213944302`  
		Last Modified: Tue, 23 Jul 2024 07:19:41 GMT  
		Size: 67.9 MB (67893807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bbc4ae6f356e392cb815fd42aba13d9a9f36c4436fb275354e2f197b00d07a`  
		Last Modified: Tue, 23 Jul 2024 07:19:39 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2` - unknown; unknown

```console
$ docker pull emqx@sha256:e2c3cab821f3f894eec87ae1863d037cc10322134d716547549343cbffa53cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2821478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa1c15416fb1786bc7543097c7f7b8010d8c8cbc54e12942b6753629dd03d03`

```dockerfile
```

-	Layers:
	-	`sha256:d5cf5699c22d1a5b4d40ae217257d78a85cdec49ea0c6b53870da496b9539ea9`  
		Last Modified: Tue, 23 Jul 2024 07:19:39 GMT  
		Size: 2.8 MB (2805848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf7cff96c7e01c881669b333a116bc618e611c3c531cd121ed3f096ff4484e4`  
		Last Modified: Tue, 23 Jul 2024 07:19:38 GMT  
		Size: 15.6 KB (15630 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2708e71ad3f057b1775c082667e25d73ba3941d133daa30f0ad874a4f26080eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91262048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0107bda72433d36425f8cd1d2d868bf32be91c2feb3be03518b2a4db450566ad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6954b87d9e796a5f22ed4a29baf172985eb4f0a9d8bdca08b8e94c438eb6590e`  
		Last Modified: Tue, 23 Jul 2024 14:00:58 GMT  
		Size: 1.6 MB (1643731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6913576463f30d88ea77bf249451d153a6c7c4ad3e2bea88dfaca2b0eacdd7d`  
		Last Modified: Tue, 23 Jul 2024 14:00:57 GMT  
		Size: 4.0 KB (3993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90286686b219216b58c270f3c666850676e9f17e83fbf5edee741695b8a7a373`  
		Last Modified: Tue, 23 Jul 2024 14:00:59 GMT  
		Size: 59.5 MB (59537309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307e77e865e462f69a9d10122c2404f67231ddc188f2f96fcd5999a43ade3bf`  
		Last Modified: Tue, 23 Jul 2024 14:00:58 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2` - unknown; unknown

```console
$ docker pull emqx@sha256:0da567b1a3f97622f5548b02fcae29755ca5dba01587a15261b36756bd6b9ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2821992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e424d14d3194eb2fe3d9c6efa06f06a31624d9f553adc2da6a4d7dbf998f2bf6`

```dockerfile
```

-	Layers:
	-	`sha256:b0c7c2900f70f0272d5ddbf93a2f122630077e14e69e8f623ec498b445d6dec5`  
		Last Modified: Tue, 23 Jul 2024 14:00:58 GMT  
		Size: 2.8 MB (2806083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a1a6742514c525d5ccc4744219c1b0f5cda98d3122a83b7626ecf229dfc2a07`  
		Last Modified: Tue, 23 Jul 2024 14:00:57 GMT  
		Size: 15.9 KB (15909 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:8841fd92e6398e9ebf8d048d1944ae404ef0b062e0526706045e9e28f65d387e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:a0849341eebb70b49fee29b693f9f123565dc4691a06de9e044459e467389e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (100956082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7a55867b2cd375ce93ac98c4df13776b6e900607d423711ebd61cf58188e64`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e189bca6085d98f7f8cbed0ab1b2102a4d2aac5a5e572323ccefc7fbe5ecdd3`  
		Last Modified: Tue, 23 Jul 2024 07:19:39 GMT  
		Size: 1.6 MB (1629027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba433d75d4bd1f3423515cbba9d3255248e2c6341dda4b1d9c38d0f22e9d822c`  
		Last Modified: Tue, 23 Jul 2024 07:19:38 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf15f68a2f2cd2e73ad2aea4fd6c47b28de391809b83cec9471e70a213944302`  
		Last Modified: Tue, 23 Jul 2024 07:19:41 GMT  
		Size: 67.9 MB (67893807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bbc4ae6f356e392cb815fd42aba13d9a9f36c4436fb275354e2f197b00d07a`  
		Last Modified: Tue, 23 Jul 2024 07:19:39 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2.1` - unknown; unknown

```console
$ docker pull emqx@sha256:e2c3cab821f3f894eec87ae1863d037cc10322134d716547549343cbffa53cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2821478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa1c15416fb1786bc7543097c7f7b8010d8c8cbc54e12942b6753629dd03d03`

```dockerfile
```

-	Layers:
	-	`sha256:d5cf5699c22d1a5b4d40ae217257d78a85cdec49ea0c6b53870da496b9539ea9`  
		Last Modified: Tue, 23 Jul 2024 07:19:39 GMT  
		Size: 2.8 MB (2805848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf7cff96c7e01c881669b333a116bc618e611c3c531cd121ed3f096ff4484e4`  
		Last Modified: Tue, 23 Jul 2024 07:19:38 GMT  
		Size: 15.6 KB (15630 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.2.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2708e71ad3f057b1775c082667e25d73ba3941d133daa30f0ad874a4f26080eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91262048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0107bda72433d36425f8cd1d2d868bf32be91c2feb3be03518b2a4db450566ad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6954b87d9e796a5f22ed4a29baf172985eb4f0a9d8bdca08b8e94c438eb6590e`  
		Last Modified: Tue, 23 Jul 2024 14:00:58 GMT  
		Size: 1.6 MB (1643731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6913576463f30d88ea77bf249451d153a6c7c4ad3e2bea88dfaca2b0eacdd7d`  
		Last Modified: Tue, 23 Jul 2024 14:00:57 GMT  
		Size: 4.0 KB (3993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90286686b219216b58c270f3c666850676e9f17e83fbf5edee741695b8a7a373`  
		Last Modified: Tue, 23 Jul 2024 14:00:59 GMT  
		Size: 59.5 MB (59537309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e307e77e865e462f69a9d10122c2404f67231ddc188f2f96fcd5999a43ade3bf`  
		Last Modified: Tue, 23 Jul 2024 14:00:58 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2.1` - unknown; unknown

```console
$ docker pull emqx@sha256:0da567b1a3f97622f5548b02fcae29755ca5dba01587a15261b36756bd6b9ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2821992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e424d14d3194eb2fe3d9c6efa06f06a31624d9f553adc2da6a4d7dbf998f2bf6`

```dockerfile
```

-	Layers:
	-	`sha256:b0c7c2900f70f0272d5ddbf93a2f122630077e14e69e8f623ec498b445d6dec5`  
		Last Modified: Tue, 23 Jul 2024 14:00:58 GMT  
		Size: 2.8 MB (2806083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a1a6742514c525d5ccc4744219c1b0f5cda98d3122a83b7626ecf229dfc2a07`  
		Last Modified: Tue, 23 Jul 2024 14:00:57 GMT  
		Size: 15.9 KB (15909 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.3`

```console
$ docker pull emqx@sha256:327c35198814877bb8fa204d06e353bc215d812918a1227ce08615fa0b48264e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:a6fe3c0c2168a117cd1fb144446715cae592b1d40b4f7d83506cdb78bec151ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101788638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd370770950487b90d8130e5dafe4a0462c21838af82ba085470a4f07613446e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e331474f7851debe45007e158fdcd7f49976b79070bec20e5ceba179bf9aaca3`  
		Last Modified: Tue, 23 Jul 2024 07:19:37 GMT  
		Size: 70.4 MB (70359376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2899f845418245006d6927a3b61d29a1693efc77385165598ad5e6292b474337`  
		Last Modified: Tue, 23 Jul 2024 07:19:34 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3` - unknown; unknown

```console
$ docker pull emqx@sha256:f645d17309997cf898cd4906ea20f63db739510f07911f1abe96e943229bda5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7517e06fe5c6e863ad826476f4b4927bbdf7316b3d01dc3f441a9643748828f`

```dockerfile
```

-	Layers:
	-	`sha256:71c51d352ef22c8160dffbd058bf8adf08a3698941e1b2b92565f07b5a3100e2`  
		Last Modified: Tue, 23 Jul 2024 07:19:35 GMT  
		Size: 2.8 MB (2817191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a131d85add3520004ebfadb1510e09b8349b2e71e0a257ee843531f808aa7e`  
		Last Modified: Tue, 23 Jul 2024 07:19:34 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:0b7dd22e7bd558d2acc8ee6b5e8da90cd4ec61ab7e3eedfd0ef5a5779c2ad5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92087552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4719e7f0e8e83fd6105f5b72d45262f7a1346c8d8bac26e46e4f8e60adc4830b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471f74e0540d331be05920e4ac4526419c0789958840d25c34ccd94cfaae7b5d`  
		Last Modified: Tue, 23 Jul 2024 14:01:36 GMT  
		Size: 62.0 MB (62010537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4418c90517ddae599f866742bd78aa31f7cab6e0b5c4605b1603371149752088`  
		Last Modified: Tue, 23 Jul 2024 14:01:34 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3` - unknown; unknown

```console
$ docker pull emqx@sha256:2ba8eab3c8fb7b74d3c03d4ce85a7ac92df34b7bb3adf617a27d843ebcb9ed0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2830264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa25b678336c82eda41f10750bbc3370c9d3e52415f701c3452a45393cfa64f9`

```dockerfile
```

-	Layers:
	-	`sha256:f31b7bda7469e75289fb5aaaff33fe2d9b21be31481f5400eec7ffe2b375d917`  
		Last Modified: Tue, 23 Jul 2024 14:01:35 GMT  
		Size: 2.8 MB (2817426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eecfcdf7121c738f6fed85d64c9cadf1d262f2a70a5a7a3d81f9f5b99c66f09`  
		Last Modified: Tue, 23 Jul 2024 14:01:34 GMT  
		Size: 12.8 KB (12838 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:327c35198814877bb8fa204d06e353bc215d812918a1227ce08615fa0b48264e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:a6fe3c0c2168a117cd1fb144446715cae592b1d40b4f7d83506cdb78bec151ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101788638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd370770950487b90d8130e5dafe4a0462c21838af82ba085470a4f07613446e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e331474f7851debe45007e158fdcd7f49976b79070bec20e5ceba179bf9aaca3`  
		Last Modified: Tue, 23 Jul 2024 07:19:37 GMT  
		Size: 70.4 MB (70359376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2899f845418245006d6927a3b61d29a1693efc77385165598ad5e6292b474337`  
		Last Modified: Tue, 23 Jul 2024 07:19:34 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3.2` - unknown; unknown

```console
$ docker pull emqx@sha256:f645d17309997cf898cd4906ea20f63db739510f07911f1abe96e943229bda5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7517e06fe5c6e863ad826476f4b4927bbdf7316b3d01dc3f441a9643748828f`

```dockerfile
```

-	Layers:
	-	`sha256:71c51d352ef22c8160dffbd058bf8adf08a3698941e1b2b92565f07b5a3100e2`  
		Last Modified: Tue, 23 Jul 2024 07:19:35 GMT  
		Size: 2.8 MB (2817191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a131d85add3520004ebfadb1510e09b8349b2e71e0a257ee843531f808aa7e`  
		Last Modified: Tue, 23 Jul 2024 07:19:34 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.3.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:0b7dd22e7bd558d2acc8ee6b5e8da90cd4ec61ab7e3eedfd0ef5a5779c2ad5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92087552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4719e7f0e8e83fd6105f5b72d45262f7a1346c8d8bac26e46e4f8e60adc4830b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471f74e0540d331be05920e4ac4526419c0789958840d25c34ccd94cfaae7b5d`  
		Last Modified: Tue, 23 Jul 2024 14:01:36 GMT  
		Size: 62.0 MB (62010537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4418c90517ddae599f866742bd78aa31f7cab6e0b5c4605b1603371149752088`  
		Last Modified: Tue, 23 Jul 2024 14:01:34 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3.2` - unknown; unknown

```console
$ docker pull emqx@sha256:2ba8eab3c8fb7b74d3c03d4ce85a7ac92df34b7bb3adf617a27d843ebcb9ed0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2830264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa25b678336c82eda41f10750bbc3370c9d3e52415f701c3452a45393cfa64f9`

```dockerfile
```

-	Layers:
	-	`sha256:f31b7bda7469e75289fb5aaaff33fe2d9b21be31481f5400eec7ffe2b375d917`  
		Last Modified: Tue, 23 Jul 2024 14:01:35 GMT  
		Size: 2.8 MB (2817426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eecfcdf7121c738f6fed85d64c9cadf1d262f2a70a5a7a3d81f9f5b99c66f09`  
		Last Modified: Tue, 23 Jul 2024 14:01:34 GMT  
		Size: 12.8 KB (12838 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.4`

```console
$ docker pull emqx@sha256:04d3b7db563c27e2079012c965ab5b779b3370e4593ede58b39d71f380e702ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.4` - linux; amd64

```console
$ docker pull emqx@sha256:262777adf23fd79cd9ad8483c944e75f066a5350f084cfa81c1a0544496653f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118702428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18197ba4751815032809d286a6188ab366c189483c8183136296c2c2fbede8a6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea714ba9b9d35e53b7b7b219714cd5d47d607621fbe17f648e006cd41997bacd`  
		Last Modified: Tue, 23 Jul 2024 07:19:41 GMT  
		Size: 87.3 MB (87273168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e491635fe7358b221ac87cec318fe90c38d981d1214a2908d5c62c37c5dd1e8d`  
		Last Modified: Tue, 23 Jul 2024 07:19:40 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4` - unknown; unknown

```console
$ docker pull emqx@sha256:26e70fe1933e641c84e20bfe6bc2ace9db7f7b719a375f7e48082edd21f22706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbed9f965307bd8bf1d792e340d0b97df8f44ebec6ad308fb4d89affc44d046`

```dockerfile
```

-	Layers:
	-	`sha256:4301c76f3e24f16ab4fc68b97bc25902ffa96c7a13a4e0118b04bc85fb5d15dd`  
		Last Modified: Tue, 23 Jul 2024 07:19:40 GMT  
		Size: 2.8 MB (2810516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d3c7f0f2b38e8b4470a688648ee89239ea7da80f39dcc0288de81937f01d89`  
		Last Modified: Tue, 23 Jul 2024 07:19:40 GMT  
		Size: 12.5 KB (12502 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f073d05019df0f450eda046b894c6e24289946380b0dde2119246f85aa1d66e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108486009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac10de7a738b5d3b381c88c993895de0e7a3576df48ec434fc429fc1bc39a953`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123873dd20fc824026b1c9bad34fde942d9df950a8708621ce1581c7437a1587`  
		Last Modified: Tue, 23 Jul 2024 14:02:15 GMT  
		Size: 78.4 MB (78408995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f23539ef7cd372705aeb96bcff18c3a55e5d0aa228329bdd8e4f4210eb9407`  
		Last Modified: Tue, 23 Jul 2024 14:02:12 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4` - unknown; unknown

```console
$ docker pull emqx@sha256:477b5fa82c8e8d2501620801e859cf69b5c66a26f3675e30a48870f87d7ea5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49bc6c65b1b8598a03cd161fabfb8292e0399c2813a807f34f736a0a108aab6`

```dockerfile
```

-	Layers:
	-	`sha256:8600cf659bb744d15dfe4479789b91f0e7cd650b9cebc21b606b12e57d96396b`  
		Last Modified: Tue, 23 Jul 2024 14:02:12 GMT  
		Size: 2.8 MB (2810751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74e59b4314eaeac790cc184e82352350aeaf470f811799acbbe451e51f55b57c`  
		Last Modified: Tue, 23 Jul 2024 14:02:12 GMT  
		Size: 12.8 KB (12782 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.4.1`

```console
$ docker pull emqx@sha256:04d3b7db563c27e2079012c965ab5b779b3370e4593ede58b39d71f380e702ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.4.1` - linux; amd64

```console
$ docker pull emqx@sha256:262777adf23fd79cd9ad8483c944e75f066a5350f084cfa81c1a0544496653f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118702428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18197ba4751815032809d286a6188ab366c189483c8183136296c2c2fbede8a6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea714ba9b9d35e53b7b7b219714cd5d47d607621fbe17f648e006cd41997bacd`  
		Last Modified: Tue, 23 Jul 2024 07:19:41 GMT  
		Size: 87.3 MB (87273168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e491635fe7358b221ac87cec318fe90c38d981d1214a2908d5c62c37c5dd1e8d`  
		Last Modified: Tue, 23 Jul 2024 07:19:40 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4.1` - unknown; unknown

```console
$ docker pull emqx@sha256:26e70fe1933e641c84e20bfe6bc2ace9db7f7b719a375f7e48082edd21f22706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbed9f965307bd8bf1d792e340d0b97df8f44ebec6ad308fb4d89affc44d046`

```dockerfile
```

-	Layers:
	-	`sha256:4301c76f3e24f16ab4fc68b97bc25902ffa96c7a13a4e0118b04bc85fb5d15dd`  
		Last Modified: Tue, 23 Jul 2024 07:19:40 GMT  
		Size: 2.8 MB (2810516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d3c7f0f2b38e8b4470a688648ee89239ea7da80f39dcc0288de81937f01d89`  
		Last Modified: Tue, 23 Jul 2024 07:19:40 GMT  
		Size: 12.5 KB (12502 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.4.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f073d05019df0f450eda046b894c6e24289946380b0dde2119246f85aa1d66e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108486009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac10de7a738b5d3b381c88c993895de0e7a3576df48ec434fc429fc1bc39a953`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123873dd20fc824026b1c9bad34fde942d9df950a8708621ce1581c7437a1587`  
		Last Modified: Tue, 23 Jul 2024 14:02:15 GMT  
		Size: 78.4 MB (78408995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f23539ef7cd372705aeb96bcff18c3a55e5d0aa228329bdd8e4f4210eb9407`  
		Last Modified: Tue, 23 Jul 2024 14:02:12 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4.1` - unknown; unknown

```console
$ docker pull emqx@sha256:477b5fa82c8e8d2501620801e859cf69b5c66a26f3675e30a48870f87d7ea5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49bc6c65b1b8598a03cd161fabfb8292e0399c2813a807f34f736a0a108aab6`

```dockerfile
```

-	Layers:
	-	`sha256:8600cf659bb744d15dfe4479789b91f0e7cd650b9cebc21b606b12e57d96396b`  
		Last Modified: Tue, 23 Jul 2024 14:02:12 GMT  
		Size: 2.8 MB (2810751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74e59b4314eaeac790cc184e82352350aeaf470f811799acbbe451e51f55b57c`  
		Last Modified: Tue, 23 Jul 2024 14:02:12 GMT  
		Size: 12.8 KB (12782 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.5`

```console
$ docker pull emqx@sha256:4e074159996273326808d9c74ca222fae31eb229cbbaaabb9f819f4a4b88acfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.5` - linux; amd64

```console
$ docker pull emqx@sha256:d5f2cb2a5502757eba734c225cdb184cc6a8730bb511157e3bbe2e056e0d3024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121268622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d314375323dde3608b960c3945617a227981386ab755843f8398202ebb7819`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6404f8ff86888fd6c35089c5bd704c38ef0605c8a8ce905a3524b656003fe8b5`  
		Last Modified: Tue, 23 Jul 2024 07:19:39 GMT  
		Size: 89.8 MB (89839229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef18a9365b7f384b5e01a202bbba4d12664d019282cc89130608da8f1e4dad0d`  
		Last Modified: Tue, 23 Jul 2024 07:19:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5` - unknown; unknown

```console
$ docker pull emqx@sha256:7baffabd412d6360aaf075abf42876c48d64785fc6ee447e6cdde5f9337b6e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0adb12e0ab236b5bacc29103cc97f6640aee8ffa6a43395270d4ea841f92b08`

```dockerfile
```

-	Layers:
	-	`sha256:b378b471d429c4426abbd08382ef61722d20dc5092766ee7354839fd18a9c0f5`  
		Last Modified: Tue, 23 Jul 2024 07:19:37 GMT  
		Size: 2.8 MB (2810477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea5a377f056dfec42047ac3dfdd3075d88964aa8f502faf12e8316b40f7e9b04`  
		Last Modified: Tue, 23 Jul 2024 07:19:37 GMT  
		Size: 12.6 KB (12605 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8121ca5fa4c2be272dba31e17e6536d0ec3ad1032eb8a0f5d608d20e6a7aaede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116784261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289d4e2212b87ed3c6d0fce8d887a2d5cf20bfb704e6c9c2ef602a443d500b6a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4d08c21eb1483b3f8a8fffdbcb6d56de937291ca274ff0a9833ce017c309a8`  
		Last Modified: Tue, 23 Jul 2024 14:02:57 GMT  
		Size: 86.7 MB (86707113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1785222cfb0a1006e272577ee9b2b1da140c0d1b657f7519927c756dc484ac73`  
		Last Modified: Tue, 23 Jul 2024 14:02:54 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5` - unknown; unknown

```console
$ docker pull emqx@sha256:e60fba8aa2017b2743dda495f9cd88de88a0c779fd08879b80f4c18505bae97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b2112c3cb13c17266562d22c545ee9641987463dc37669d2f18e819210efe5`

```dockerfile
```

-	Layers:
	-	`sha256:2a4e3e81fcd9a993cdc19921227315c848b42a77f8045fcca2a466e1ef837318`  
		Last Modified: Tue, 23 Jul 2024 14:02:55 GMT  
		Size: 2.8 MB (2810712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5071be4ae1301a658603e70b7ae8c4ce7e9d6d36e93dffa378fcf65623c885db`  
		Last Modified: Tue, 23 Jul 2024 14:02:55 GMT  
		Size: 12.9 KB (12884 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.5.1`

```console
$ docker pull emqx@sha256:4e074159996273326808d9c74ca222fae31eb229cbbaaabb9f819f4a4b88acfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.5.1` - linux; amd64

```console
$ docker pull emqx@sha256:d5f2cb2a5502757eba734c225cdb184cc6a8730bb511157e3bbe2e056e0d3024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121268622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d314375323dde3608b960c3945617a227981386ab755843f8398202ebb7819`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6404f8ff86888fd6c35089c5bd704c38ef0605c8a8ce905a3524b656003fe8b5`  
		Last Modified: Tue, 23 Jul 2024 07:19:39 GMT  
		Size: 89.8 MB (89839229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef18a9365b7f384b5e01a202bbba4d12664d019282cc89130608da8f1e4dad0d`  
		Last Modified: Tue, 23 Jul 2024 07:19:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:7baffabd412d6360aaf075abf42876c48d64785fc6ee447e6cdde5f9337b6e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0adb12e0ab236b5bacc29103cc97f6640aee8ffa6a43395270d4ea841f92b08`

```dockerfile
```

-	Layers:
	-	`sha256:b378b471d429c4426abbd08382ef61722d20dc5092766ee7354839fd18a9c0f5`  
		Last Modified: Tue, 23 Jul 2024 07:19:37 GMT  
		Size: 2.8 MB (2810477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea5a377f056dfec42047ac3dfdd3075d88964aa8f502faf12e8316b40f7e9b04`  
		Last Modified: Tue, 23 Jul 2024 07:19:37 GMT  
		Size: 12.6 KB (12605 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8121ca5fa4c2be272dba31e17e6536d0ec3ad1032eb8a0f5d608d20e6a7aaede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116784261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289d4e2212b87ed3c6d0fce8d887a2d5cf20bfb704e6c9c2ef602a443d500b6a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4d08c21eb1483b3f8a8fffdbcb6d56de937291ca274ff0a9833ce017c309a8`  
		Last Modified: Tue, 23 Jul 2024 14:02:57 GMT  
		Size: 86.7 MB (86707113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1785222cfb0a1006e272577ee9b2b1da140c0d1b657f7519927c756dc484ac73`  
		Last Modified: Tue, 23 Jul 2024 14:02:54 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:e60fba8aa2017b2743dda495f9cd88de88a0c779fd08879b80f4c18505bae97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b2112c3cb13c17266562d22c545ee9641987463dc37669d2f18e819210efe5`

```dockerfile
```

-	Layers:
	-	`sha256:2a4e3e81fcd9a993cdc19921227315c848b42a77f8045fcca2a466e1ef837318`  
		Last Modified: Tue, 23 Jul 2024 14:02:55 GMT  
		Size: 2.8 MB (2810712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5071be4ae1301a658603e70b7ae8c4ce7e9d6d36e93dffa378fcf65623c885db`  
		Last Modified: Tue, 23 Jul 2024 14:02:55 GMT  
		Size: 12.9 KB (12884 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.6`

```console
$ docker pull emqx@sha256:d8fe34cadf8166fc81291dc03bf752b61f1aa666e2d5b72a776b0adab077739a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.6` - linux; amd64

```console
$ docker pull emqx@sha256:675686d706f0bc997abdf76c0acfb619a638ce47d9f0e28b790dc77e587a6ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124180948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23cce53894a9ea27727dc3c93f3baa6f56d37e4458355bcf3dcef8f69d4c7b71`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
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
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461dd64345866487ebdf19993bae617d70db890df0434a3236814f9021d81316`  
		Last Modified: Tue, 23 Jul 2024 07:19:46 GMT  
		Size: 95.1 MB (95053598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14f3a6b5697a0da8dc4f0b4d143f40a276048a4a7637ae73ee9edcb1df171cc`  
		Last Modified: Tue, 23 Jul 2024 07:19:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6` - unknown; unknown

```console
$ docker pull emqx@sha256:de786f8388623ea594e1575de843456177d34f6817d6f4021670e2d8165246d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc028b2643d7b121b3ab23b5b9c73b23a0fd8c2ee9ce4f5bdde5bd8f398a919`

```dockerfile
```

-	Layers:
	-	`sha256:e0f0104ada8dbe65bbbeec15e8402083574a9f6a69d055750a8630150a2c348c`  
		Last Modified: Tue, 23 Jul 2024 07:19:45 GMT  
		Size: 2.6 MB (2591425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a13de0cd6cfd5dc1496ce8183ba1f42f05776c3ebc0c75ba4f36d16e95351e7`  
		Last Modified: Tue, 23 Jul 2024 07:19:45 GMT  
		Size: 11.7 KB (11727 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8205840312b293a9c138c11cc72ccd071bcc74c5fb0695521c9920b39cb7463d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120774848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772d959d50a0d5704db40ef2796cc77360a2c6a40d9c39c7034bafb975b6cedf`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02b7c56d7480c26142cec5f15c8b726a77938c8678849f4c6cffc8043c1a505`  
		Last Modified: Tue, 23 Jul 2024 14:03:44 GMT  
		Size: 91.6 MB (91617215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55de4fb410040b93781cfde0f6bf0685362b47368b9b833042bca999cd296e3`  
		Last Modified: Tue, 23 Jul 2024 14:03:41 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6` - unknown; unknown

```console
$ docker pull emqx@sha256:5aae1feeb1926e18acaacf164207b586c29f8eef46e85f6b63a412e29426a30b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39291da9f1eff96d1ba1c34f8573c3284b7fd1beff001fc5c64837ecd3bb9780`

```dockerfile
```

-	Layers:
	-	`sha256:efe4e05d8d85eead8f6b33f895e2d50f668ac7c4943b30fe307da3a6c572c7ce`  
		Last Modified: Tue, 23 Jul 2024 14:03:42 GMT  
		Size: 2.6 MB (2591680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc0a81ec108c49f6fe97c997a1bff4afb7da7356a4d0bd18c74bfe53fd0a1cf0`  
		Last Modified: Tue, 23 Jul 2024 14:03:41 GMT  
		Size: 12.0 KB (12006 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.6.1`

```console
$ docker pull emqx@sha256:d8fe34cadf8166fc81291dc03bf752b61f1aa666e2d5b72a776b0adab077739a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.6.1` - linux; amd64

```console
$ docker pull emqx@sha256:675686d706f0bc997abdf76c0acfb619a638ce47d9f0e28b790dc77e587a6ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124180948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23cce53894a9ea27727dc3c93f3baa6f56d37e4458355bcf3dcef8f69d4c7b71`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
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
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461dd64345866487ebdf19993bae617d70db890df0434a3236814f9021d81316`  
		Last Modified: Tue, 23 Jul 2024 07:19:46 GMT  
		Size: 95.1 MB (95053598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14f3a6b5697a0da8dc4f0b4d143f40a276048a4a7637ae73ee9edcb1df171cc`  
		Last Modified: Tue, 23 Jul 2024 07:19:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6.1` - unknown; unknown

```console
$ docker pull emqx@sha256:de786f8388623ea594e1575de843456177d34f6817d6f4021670e2d8165246d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc028b2643d7b121b3ab23b5b9c73b23a0fd8c2ee9ce4f5bdde5bd8f398a919`

```dockerfile
```

-	Layers:
	-	`sha256:e0f0104ada8dbe65bbbeec15e8402083574a9f6a69d055750a8630150a2c348c`  
		Last Modified: Tue, 23 Jul 2024 07:19:45 GMT  
		Size: 2.6 MB (2591425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a13de0cd6cfd5dc1496ce8183ba1f42f05776c3ebc0c75ba4f36d16e95351e7`  
		Last Modified: Tue, 23 Jul 2024 07:19:45 GMT  
		Size: 11.7 KB (11727 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.6.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8205840312b293a9c138c11cc72ccd071bcc74c5fb0695521c9920b39cb7463d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120774848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772d959d50a0d5704db40ef2796cc77360a2c6a40d9c39c7034bafb975b6cedf`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02b7c56d7480c26142cec5f15c8b726a77938c8678849f4c6cffc8043c1a505`  
		Last Modified: Tue, 23 Jul 2024 14:03:44 GMT  
		Size: 91.6 MB (91617215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55de4fb410040b93781cfde0f6bf0685362b47368b9b833042bca999cd296e3`  
		Last Modified: Tue, 23 Jul 2024 14:03:41 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6.1` - unknown; unknown

```console
$ docker pull emqx@sha256:5aae1feeb1926e18acaacf164207b586c29f8eef46e85f6b63a412e29426a30b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39291da9f1eff96d1ba1c34f8573c3284b7fd1beff001fc5c64837ecd3bb9780`

```dockerfile
```

-	Layers:
	-	`sha256:efe4e05d8d85eead8f6b33f895e2d50f668ac7c4943b30fe307da3a6c572c7ce`  
		Last Modified: Tue, 23 Jul 2024 14:03:42 GMT  
		Size: 2.6 MB (2591680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc0a81ec108c49f6fe97c997a1bff4afb7da7356a4d0bd18c74bfe53fd0a1cf0`  
		Last Modified: Tue, 23 Jul 2024 14:03:41 GMT  
		Size: 12.0 KB (12006 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:49ac9b12a15b7e649ceb25bd74d4c7a98209ffb9b1f58da6caa1b984e6a7fa99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:66c1f31561788effe34d9804299758d4927b7e11d8467297de202a96835f925f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126238122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fdc5370bf923bab8c90743b24666bca939fd1f2874c786e47d23fa1fbbfd87b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ea6242b71c16ce1352fcf57a0d11687c2bd0b9fd496834fd62f76dd8f5ebf2`  
		Last Modified: Tue, 23 Jul 2024 07:19:54 GMT  
		Size: 97.1 MB (97110772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312a74d0107a3ee33685af3838ac090917b45e87cb3006fc6192781d92482b4c`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:8e4ad0134f93a3a02b2167fa3392b9b80c19466227b895ce27358ee2077c37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f34cd44ade291f177d0677daa06c10214702867382053ae2ca28173d626e3f8`

```dockerfile
```

-	Layers:
	-	`sha256:7c83086fd6007886c99a90d7d357091c7e561d320beb2faba0c8bbcc497c6298`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 2.6 MB (2599757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4740c9a8c3c0fdbc38c099b4759c70dc685a1bdf61a78e9702f2e6540074d6fb`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:42fa6f5d51dd4ba31bb04c74579f94fb5b542d77f5c343e9c3228bd402e08a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122815516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d420029c6f6de2a2cba1437cbc6c2f0d54ad2b6d9b6f8d3b660bcd5e238f532d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3e2f4ab829a4ca9b003191cf0f7790b7f8a4ba88d1280ba1684b699b851a0f`  
		Last Modified: Tue, 23 Jul 2024 14:04:27 GMT  
		Size: 93.7 MB (93657881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7625bfd2ba9540151b7b03e0b66859a72db79e36e53e00ab542042e1239151`  
		Last Modified: Tue, 23 Jul 2024 14:04:25 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:c6a2b798d31866b3c57031fcc0f821d0d35f020673432ae507f1d3c3dfcd4334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03008f242bed4c64734934401a004fa899a10db53a69d1981ad7d1b24aa96d5`

```dockerfile
```

-	Layers:
	-	`sha256:16d279b421c442fa999b969231f6f8aab5a32a6e8b2e9ff61d0e93303a2ad438`  
		Last Modified: Tue, 23 Jul 2024 14:04:27 GMT  
		Size: 2.6 MB (2600036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62bbf9793a6fc5236d608a0a2aaf60339a8304868e0553b4269ca7e3da7f387f`  
		Last Modified: Tue, 23 Jul 2024 14:04:25 GMT  
		Size: 12.6 KB (12608 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `emqx:latest`

```console
$ docker pull emqx@sha256:49ac9b12a15b7e649ceb25bd74d4c7a98209ffb9b1f58da6caa1b984e6a7fa99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:66c1f31561788effe34d9804299758d4927b7e11d8467297de202a96835f925f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126238122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fdc5370bf923bab8c90743b24666bca939fd1f2874c786e47d23fa1fbbfd87b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ea6242b71c16ce1352fcf57a0d11687c2bd0b9fd496834fd62f76dd8f5ebf2`  
		Last Modified: Tue, 23 Jul 2024 07:19:54 GMT  
		Size: 97.1 MB (97110772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312a74d0107a3ee33685af3838ac090917b45e87cb3006fc6192781d92482b4c`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:8e4ad0134f93a3a02b2167fa3392b9b80c19466227b895ce27358ee2077c37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f34cd44ade291f177d0677daa06c10214702867382053ae2ca28173d626e3f8`

```dockerfile
```

-	Layers:
	-	`sha256:7c83086fd6007886c99a90d7d357091c7e561d320beb2faba0c8bbcc497c6298`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 2.6 MB (2599757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4740c9a8c3c0fdbc38c099b4759c70dc685a1bdf61a78e9702f2e6540074d6fb`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:42fa6f5d51dd4ba31bb04c74579f94fb5b542d77f5c343e9c3228bd402e08a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122815516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d420029c6f6de2a2cba1437cbc6c2f0d54ad2b6d9b6f8d3b660bcd5e238f532d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3e2f4ab829a4ca9b003191cf0f7790b7f8a4ba88d1280ba1684b699b851a0f`  
		Last Modified: Tue, 23 Jul 2024 14:04:27 GMT  
		Size: 93.7 MB (93657881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7625bfd2ba9540151b7b03e0b66859a72db79e36e53e00ab542042e1239151`  
		Last Modified: Tue, 23 Jul 2024 14:04:25 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:c6a2b798d31866b3c57031fcc0f821d0d35f020673432ae507f1d3c3dfcd4334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03008f242bed4c64734934401a004fa899a10db53a69d1981ad7d1b24aa96d5`

```dockerfile
```

-	Layers:
	-	`sha256:16d279b421c442fa999b969231f6f8aab5a32a6e8b2e9ff61d0e93303a2ad438`  
		Last Modified: Tue, 23 Jul 2024 14:04:27 GMT  
		Size: 2.6 MB (2600036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62bbf9793a6fc5236d608a0a2aaf60339a8304868e0553b4269ca7e3da7f387f`  
		Last Modified: Tue, 23 Jul 2024 14:04:25 GMT  
		Size: 12.6 KB (12608 bytes)  
		MIME: application/vnd.in-toto+json
