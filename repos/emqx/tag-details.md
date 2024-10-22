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
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.1`](#emqx581)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:983d885bc1b76818bb769b1a1f4b8d713e7284e3ba72f931dc622cb4f97bfcfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:73f08b2ec0fb38e8c6b5222d2031058f92bae434e7781710f66f23f3de5dd2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109909273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c07a2f6f89b0a41ceb960016e53260246391c1ab3809ea8b1bf34e5e8f79310`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9001c341bcd760753ca192f57aac4c3ca6fe825b997840e0c18c72be1918b846`  
		Last Modified: Tue, 22 Oct 2024 16:56:08 GMT  
		Size: 80.8 MB (80781921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6d3bf26a86d0be8a04317b104743cef6703e83474b5dce305c1224feb82b4a`  
		Last Modified: Tue, 22 Oct 2024 16:56:06 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:2825e8d0751787152a7b58a9df04c82cdb4ee14e63a0b6a66b84490578ec6523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e15900551528293de41105bd08e012a64b57684f45c442d67b625e48a6dc4b8`

```dockerfile
```

-	Layers:
	-	`sha256:dcc3d0d5953a5fcf16da7dcada7a76eb83a75caf0345a35b14ba0a91978afb0f`  
		Last Modified: Tue, 22 Oct 2024 16:56:06 GMT  
		Size: 2.6 MB (2624750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb19138927642c0126a5d50f64367e4fc24e72878dde16f28c07a091b1d2a8f7`  
		Last Modified: Tue, 22 Oct 2024 16:56:06 GMT  
		Size: 12.3 KB (12315 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:bf84a3fdb8b744f65cc83b078fe6f6bbc09eac84de5c2c2d257cee6d0b2b65fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107097129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32632f41a7369effd68aa93f80c8a37c96bc903fe868f0e38de6fb9e2fba076d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d196bcfe1e1b9d831f9206be1909867be476ebcc4cd14abf81cc717c29d7274a`  
		Last Modified: Tue, 22 Oct 2024 16:55:57 GMT  
		Size: 77.9 MB (77939724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c5321e15b65b59f02dfcb34cd289b3fff03c36a88b952fb2dcb95a257a524d`  
		Last Modified: Tue, 22 Oct 2024 16:55:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:285fbd3d644a00c7a1e9426c8ecbb2642f5dc8752c49f7a06099b11cdbd9012a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84222ce87ed3bdeb1128239b1854b6149b40427373de46897280f30b997cc808`

```dockerfile
```

-	Layers:
	-	`sha256:a06dcdbccb3564a9fde3d56f720598ebc16df41eb292bbc083e813bdf7c8b299`  
		Last Modified: Tue, 22 Oct 2024 16:55:55 GMT  
		Size: 2.6 MB (2625029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bccbfcfd1900f2bab668677abbdc31bd269ea5c79d3d821c6bccc538d669d6bd`  
		Last Modified: Tue, 22 Oct 2024 16:55:55 GMT  
		Size: 12.4 KB (12437 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.1`

```console
$ docker pull emqx@sha256:5996d16f2ae4c49cfaeae423c333fa535ebdc0088e61c0e3c0d7a277cb82a29e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:15569d48de5b8a38d14a891f67769f6daf4d212e89939a5ef92b7e62d709aebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102402144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42e36699991c8eb89019e19bc1def13f3e34a50abacae0b55752dcba484948`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b75a47d61e2321e04114d7115d3d8a7444bccf6a531afa52b154abbd01bf9a1`  
		Last Modified: Thu, 17 Oct 2024 01:13:34 GMT  
		Size: 3.0 MB (2987838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce674f9128734d0dfe24ff56f7f21ab41a3cd2b51dc888cb50b42626019a7649`  
		Last Modified: Thu, 17 Oct 2024 01:13:34 GMT  
		Size: 4.0 KB (3987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0695b46fe4257c3d49554d4fdd99f051e9ae2d7eee5d6043129f3d26eb6d8d`  
		Last Modified: Thu, 17 Oct 2024 01:13:35 GMT  
		Size: 68.0 MB (67980588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d75abb4fcfd751951329cf4e3f01909c43c01fc01dea37dca7da85e69edde1d`  
		Last Modified: Thu, 17 Oct 2024 01:13:34 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:efec885b4349b0eb3c1ab7575f7a2c5028b8aded63ae627dbcd62ffc5bed94ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2876937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a735e52bdfa21b50b84b792b596b497df6f8b61e6cfae721a0fe2eca0f1def2`

```dockerfile
```

-	Layers:
	-	`sha256:cf422a6c4d67ca1a520e54b44d3aa9f4aa3d4222ae4aa7b85e9a398c68802f54`  
		Last Modified: Thu, 17 Oct 2024 01:13:34 GMT  
		Size: 2.9 MB (2861771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a005e769958f740064c3c3bf01f5eae1dd6e64e3c185e3cfbf646e887c83eee6`  
		Last Modified: Thu, 17 Oct 2024 01:13:33 GMT  
		Size: 15.2 KB (15166 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:805cbe1e4905321e9586301bb9594955ee674063ec8dc098189c685aed58f8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92704933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f969051451f72387dc676a94d3077b214e96d918cec5900b2064aeeeed38cadb`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1923fb79afa69346bb60e4fda7d18d4123c8d07f0c991676c35bd110804578b0`  
		Last Modified: Thu, 17 Oct 2024 09:13:13 GMT  
		Size: 3.0 MB (3003916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a33a435947efb63f19c20529c9b0174e9cae2ba3133c972ab3be28fe79057a`  
		Last Modified: Thu, 17 Oct 2024 09:13:13 GMT  
		Size: 4.0 KB (3995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5289c255d4380f5e43a15040b2231aef24f1eeaa6aa8615044602859fdc62a84`  
		Last Modified: Thu, 17 Oct 2024 09:13:15 GMT  
		Size: 59.6 MB (59620332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb959f5d2ef5138835c8c36e27a1020611b16a607b9f83a804036d63e4063f99`  
		Last Modified: Thu, 17 Oct 2024 09:13:13 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:259d8c9ab6efa5982bc9b388dcde2488939b923a86e576c56ed2e593c1b176ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e999234df4bd3851f1bbcf318c5fde9715984463dcffd338fb06143accfb17f2`

```dockerfile
```

-	Layers:
	-	`sha256:c5c068e167f503c483cc4cee8ca5b0a76fd18fb2b90d90af3f280d8f86546e8b`  
		Last Modified: Thu, 17 Oct 2024 09:13:13 GMT  
		Size: 2.9 MB (2862018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fb0496b86c60b438fb3dc20c925201c8f7258ebcb060f45ac5fa51d47918535`  
		Last Modified: Thu, 17 Oct 2024 09:13:13 GMT  
		Size: 15.3 KB (15270 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:5996d16f2ae4c49cfaeae423c333fa535ebdc0088e61c0e3c0d7a277cb82a29e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:15569d48de5b8a38d14a891f67769f6daf4d212e89939a5ef92b7e62d709aebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102402144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42e36699991c8eb89019e19bc1def13f3e34a50abacae0b55752dcba484948`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b75a47d61e2321e04114d7115d3d8a7444bccf6a531afa52b154abbd01bf9a1`  
		Last Modified: Thu, 17 Oct 2024 01:13:34 GMT  
		Size: 3.0 MB (2987838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce674f9128734d0dfe24ff56f7f21ab41a3cd2b51dc888cb50b42626019a7649`  
		Last Modified: Thu, 17 Oct 2024 01:13:34 GMT  
		Size: 4.0 KB (3987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0695b46fe4257c3d49554d4fdd99f051e9ae2d7eee5d6043129f3d26eb6d8d`  
		Last Modified: Thu, 17 Oct 2024 01:13:35 GMT  
		Size: 68.0 MB (67980588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d75abb4fcfd751951329cf4e3f01909c43c01fc01dea37dca7da85e69edde1d`  
		Last Modified: Thu, 17 Oct 2024 01:13:34 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1.6` - unknown; unknown

```console
$ docker pull emqx@sha256:efec885b4349b0eb3c1ab7575f7a2c5028b8aded63ae627dbcd62ffc5bed94ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2876937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a735e52bdfa21b50b84b792b596b497df6f8b61e6cfae721a0fe2eca0f1def2`

```dockerfile
```

-	Layers:
	-	`sha256:cf422a6c4d67ca1a520e54b44d3aa9f4aa3d4222ae4aa7b85e9a398c68802f54`  
		Last Modified: Thu, 17 Oct 2024 01:13:34 GMT  
		Size: 2.9 MB (2861771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a005e769958f740064c3c3bf01f5eae1dd6e64e3c185e3cfbf646e887c83eee6`  
		Last Modified: Thu, 17 Oct 2024 01:13:33 GMT  
		Size: 15.2 KB (15166 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.1.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:805cbe1e4905321e9586301bb9594955ee674063ec8dc098189c685aed58f8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92704933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f969051451f72387dc676a94d3077b214e96d918cec5900b2064aeeeed38cadb`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1923fb79afa69346bb60e4fda7d18d4123c8d07f0c991676c35bd110804578b0`  
		Last Modified: Thu, 17 Oct 2024 09:13:13 GMT  
		Size: 3.0 MB (3003916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a33a435947efb63f19c20529c9b0174e9cae2ba3133c972ab3be28fe79057a`  
		Last Modified: Thu, 17 Oct 2024 09:13:13 GMT  
		Size: 4.0 KB (3995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5289c255d4380f5e43a15040b2231aef24f1eeaa6aa8615044602859fdc62a84`  
		Last Modified: Thu, 17 Oct 2024 09:13:15 GMT  
		Size: 59.6 MB (59620332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb959f5d2ef5138835c8c36e27a1020611b16a607b9f83a804036d63e4063f99`  
		Last Modified: Thu, 17 Oct 2024 09:13:13 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1.6` - unknown; unknown

```console
$ docker pull emqx@sha256:259d8c9ab6efa5982bc9b388dcde2488939b923a86e576c56ed2e593c1b176ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e999234df4bd3851f1bbcf318c5fde9715984463dcffd338fb06143accfb17f2`

```dockerfile
```

-	Layers:
	-	`sha256:c5c068e167f503c483cc4cee8ca5b0a76fd18fb2b90d90af3f280d8f86546e8b`  
		Last Modified: Thu, 17 Oct 2024 09:13:13 GMT  
		Size: 2.9 MB (2862018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fb0496b86c60b438fb3dc20c925201c8f7258ebcb060f45ac5fa51d47918535`  
		Last Modified: Thu, 17 Oct 2024 09:13:13 GMT  
		Size: 15.3 KB (15270 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.2`

```console
$ docker pull emqx@sha256:b33d9421fd90a58fe9572b1cfd73967b055a37950f3f77d59e46c899b7599980
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:9becaf3e3d9a371ebf9cd75f5c669b63997110e031a7e43d0f07bdbd1957a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (100956525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ebde53144a3a067bf55790593f0420710436083510f0ab4cb04a0e2e49c28e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5848e798240d5c6cce23601977d7c8bc8ae035adb81f107006c8173abf1407`  
		Last Modified: Thu, 17 Oct 2024 01:13:49 GMT  
		Size: 1.6 MB (1629044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e9d8f0e925bd8c8d37f32548adaa58fb657069fc710916e80092238c828e31`  
		Last Modified: Thu, 17 Oct 2024 01:13:48 GMT  
		Size: 4.0 KB (3988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea533794f957cc571395ff33033a012f42041b5c030cabdea16b05cbfb302eb`  
		Last Modified: Thu, 17 Oct 2024 01:13:51 GMT  
		Size: 67.9 MB (67893763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad51aacd2401d07abd455c0869ca6c20900306f95d126a998c2253fc732e408`  
		Last Modified: Thu, 17 Oct 2024 01:13:49 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2` - unknown; unknown

```console
$ docker pull emqx@sha256:dabdb9fdd986e74ecacd138c90f2a9d58e00b2d30d3d3bb9717d745dea6073a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2821619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91917ee6a5aca3672d7a1c0c9d9f76f6068444ffece8d109a8bb964a80957772`

```dockerfile
```

-	Layers:
	-	`sha256:039f2abb526bf0903e416e7f18e1c7be1a000a3a4d3d1d55138a132ca5db5e57`  
		Last Modified: Thu, 17 Oct 2024 01:13:49 GMT  
		Size: 2.8 MB (2805951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090347c5e2476da40632952931e1375c3b854ebffe7b70852f1b58f5c6be1bbe`  
		Last Modified: Thu, 17 Oct 2024 01:13:48 GMT  
		Size: 15.7 KB (15668 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:15993dba39f3783343716e7840de60777e263a0dcadd6410ad029c218a7dce2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91261562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c064aa4b41f7ff63a280a438434d0832ad88ad6cccbb6fa725007a9b5df8c8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f21a98dd947226469ece64e7653cfee0fe0229d18f82693c13cadc0159ee4e6`  
		Last Modified: Thu, 17 Oct 2024 09:13:59 GMT  
		Size: 1.6 MB (1643675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092b83738428059e0c6c37076ef771a9d68d051a2ed372dc2debf9f3499728a`  
		Last Modified: Thu, 17 Oct 2024 09:13:59 GMT  
		Size: 4.0 KB (3993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa29629b2a41f97b789d265766f168b58229b861166dea5a9871a241950bc1c`  
		Last Modified: Thu, 17 Oct 2024 09:14:01 GMT  
		Size: 59.5 MB (59537204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91fb096d1f4e13b413f3cbb312f204acc24409e322f67b706191dc3fc76fc56`  
		Last Modified: Thu, 17 Oct 2024 09:13:59 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2` - unknown; unknown

```console
$ docker pull emqx@sha256:1bfe0fa60e6818dbfba44dc2decc9b0e40129185291738b2a522f5c9c69b546a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2821958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0870f3c1012afc41b20c9518a80826540b2be0a471985082b5947666f6c8d021`

```dockerfile
```

-	Layers:
	-	`sha256:b1ce484417e9db4b95733640ad95cfc270cdcc2885a1e0ba27d319e6c79c6a97`  
		Last Modified: Thu, 17 Oct 2024 09:13:59 GMT  
		Size: 2.8 MB (2806186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86bb70805c34560d135221ff68078a49a9c4fcf1dbc97df0415856a23985e9da`  
		Last Modified: Thu, 17 Oct 2024 09:13:59 GMT  
		Size: 15.8 KB (15772 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:b33d9421fd90a58fe9572b1cfd73967b055a37950f3f77d59e46c899b7599980
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:9becaf3e3d9a371ebf9cd75f5c669b63997110e031a7e43d0f07bdbd1957a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (100956525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ebde53144a3a067bf55790593f0420710436083510f0ab4cb04a0e2e49c28e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5848e798240d5c6cce23601977d7c8bc8ae035adb81f107006c8173abf1407`  
		Last Modified: Thu, 17 Oct 2024 01:13:49 GMT  
		Size: 1.6 MB (1629044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e9d8f0e925bd8c8d37f32548adaa58fb657069fc710916e80092238c828e31`  
		Last Modified: Thu, 17 Oct 2024 01:13:48 GMT  
		Size: 4.0 KB (3988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea533794f957cc571395ff33033a012f42041b5c030cabdea16b05cbfb302eb`  
		Last Modified: Thu, 17 Oct 2024 01:13:51 GMT  
		Size: 67.9 MB (67893763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad51aacd2401d07abd455c0869ca6c20900306f95d126a998c2253fc732e408`  
		Last Modified: Thu, 17 Oct 2024 01:13:49 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2.1` - unknown; unknown

```console
$ docker pull emqx@sha256:dabdb9fdd986e74ecacd138c90f2a9d58e00b2d30d3d3bb9717d745dea6073a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2821619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91917ee6a5aca3672d7a1c0c9d9f76f6068444ffece8d109a8bb964a80957772`

```dockerfile
```

-	Layers:
	-	`sha256:039f2abb526bf0903e416e7f18e1c7be1a000a3a4d3d1d55138a132ca5db5e57`  
		Last Modified: Thu, 17 Oct 2024 01:13:49 GMT  
		Size: 2.8 MB (2805951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090347c5e2476da40632952931e1375c3b854ebffe7b70852f1b58f5c6be1bbe`  
		Last Modified: Thu, 17 Oct 2024 01:13:48 GMT  
		Size: 15.7 KB (15668 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.2.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:15993dba39f3783343716e7840de60777e263a0dcadd6410ad029c218a7dce2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91261562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c064aa4b41f7ff63a280a438434d0832ad88ad6cccbb6fa725007a9b5df8c8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f21a98dd947226469ece64e7653cfee0fe0229d18f82693c13cadc0159ee4e6`  
		Last Modified: Thu, 17 Oct 2024 09:13:59 GMT  
		Size: 1.6 MB (1643675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092b83738428059e0c6c37076ef771a9d68d051a2ed372dc2debf9f3499728a`  
		Last Modified: Thu, 17 Oct 2024 09:13:59 GMT  
		Size: 4.0 KB (3993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa29629b2a41f97b789d265766f168b58229b861166dea5a9871a241950bc1c`  
		Last Modified: Thu, 17 Oct 2024 09:14:01 GMT  
		Size: 59.5 MB (59537204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91fb096d1f4e13b413f3cbb312f204acc24409e322f67b706191dc3fc76fc56`  
		Last Modified: Thu, 17 Oct 2024 09:13:59 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2.1` - unknown; unknown

```console
$ docker pull emqx@sha256:1bfe0fa60e6818dbfba44dc2decc9b0e40129185291738b2a522f5c9c69b546a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2821958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0870f3c1012afc41b20c9518a80826540b2be0a471985082b5947666f6c8d021`

```dockerfile
```

-	Layers:
	-	`sha256:b1ce484417e9db4b95733640ad95cfc270cdcc2885a1e0ba27d319e6c79c6a97`  
		Last Modified: Thu, 17 Oct 2024 09:13:59 GMT  
		Size: 2.8 MB (2806186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86bb70805c34560d135221ff68078a49a9c4fcf1dbc97df0415856a23985e9da`  
		Last Modified: Thu, 17 Oct 2024 09:13:59 GMT  
		Size: 15.8 KB (15772 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.3`

```console
$ docker pull emqx@sha256:dddee875a39895b0ee8a3acdcc9185ccd1e6730317dab2333c1f7ee461301e68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:ac667618dc8031c5690a80281f3d0f60b1d80217cf05a43a74650420daf638a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101789174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dafd107843842a2332cd2be23c37a5cb1541c522e3e9de7a1a270cca88130fd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e600c149a22cfc8e38263c29040196802815e1b78c7630457814b53d7d249791`  
		Last Modified: Thu, 17 Oct 2024 01:13:46 GMT  
		Size: 70.4 MB (70359442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b299a05840136407c3d873c252387f202b9731a4f15509925cfb3c0b53b61c`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3` - unknown; unknown

```console
$ docker pull emqx@sha256:6e92d9e24a083279deb1f74c8f55840fa7b897b73d4108b14702cdb62f099124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bf17e58d1fb9f38d9ec986b706305644fa45523251f057ce976501b7d1aef6`

```dockerfile
```

-	Layers:
	-	`sha256:4a0b8d5ef3a55ceed3a2ba18632c01cde7202b2b5f33fc08ae45b76e66e31af2`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 2.8 MB (2817294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9a4cf972809fef08a2d550a32879fca152f1aa694670a7035761e560bba20ba`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 12.6 KB (12596 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:c60a022e55ae52804ae53f55512ca4b4da0f123eb929a1fc002a2ea42627946a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92087242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14128ae4b923a073e7e4ffe4b0b4d8b878a6b32548456ac1ae17a6093348b154`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94db5ffdad5513b2fbc3a81070f7d413514ba1a2816da4afb230a6f2b9c986b4`  
		Last Modified: Thu, 17 Oct 2024 09:14:38 GMT  
		Size: 62.0 MB (62010553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e274832f7c2be1cefce62c0f761c9e30685cb9e2599f334a712ec0bcfe41bb`  
		Last Modified: Thu, 17 Oct 2024 09:14:36 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3` - unknown; unknown

```console
$ docker pull emqx@sha256:cf01109bace3c05412f2e4dacc0de4c71941a82f3e6f1560f6ca543bb7055d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2830199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0026944e55c7139e6d592d06ee03b4220fbcf76f54927a0b7ab8929e35a1d106`

```dockerfile
```

-	Layers:
	-	`sha256:5603f89b568936a407db00a85ddc384456fc1313821d4152ddc2fbb0906f7d6c`  
		Last Modified: Thu, 17 Oct 2024 09:14:37 GMT  
		Size: 2.8 MB (2817529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b75ba5d13d9fdf7caa9a00b851a4de2fef7f188cc600e141d96ce6ea8e3b744a`  
		Last Modified: Thu, 17 Oct 2024 09:14:36 GMT  
		Size: 12.7 KB (12670 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:dddee875a39895b0ee8a3acdcc9185ccd1e6730317dab2333c1f7ee461301e68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:ac667618dc8031c5690a80281f3d0f60b1d80217cf05a43a74650420daf638a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101789174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dafd107843842a2332cd2be23c37a5cb1541c522e3e9de7a1a270cca88130fd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e600c149a22cfc8e38263c29040196802815e1b78c7630457814b53d7d249791`  
		Last Modified: Thu, 17 Oct 2024 01:13:46 GMT  
		Size: 70.4 MB (70359442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b299a05840136407c3d873c252387f202b9731a4f15509925cfb3c0b53b61c`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3.2` - unknown; unknown

```console
$ docker pull emqx@sha256:6e92d9e24a083279deb1f74c8f55840fa7b897b73d4108b14702cdb62f099124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bf17e58d1fb9f38d9ec986b706305644fa45523251f057ce976501b7d1aef6`

```dockerfile
```

-	Layers:
	-	`sha256:4a0b8d5ef3a55ceed3a2ba18632c01cde7202b2b5f33fc08ae45b76e66e31af2`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 2.8 MB (2817294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9a4cf972809fef08a2d550a32879fca152f1aa694670a7035761e560bba20ba`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 12.6 KB (12596 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.3.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:c60a022e55ae52804ae53f55512ca4b4da0f123eb929a1fc002a2ea42627946a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92087242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14128ae4b923a073e7e4ffe4b0b4d8b878a6b32548456ac1ae17a6093348b154`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94db5ffdad5513b2fbc3a81070f7d413514ba1a2816da4afb230a6f2b9c986b4`  
		Last Modified: Thu, 17 Oct 2024 09:14:38 GMT  
		Size: 62.0 MB (62010553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e274832f7c2be1cefce62c0f761c9e30685cb9e2599f334a712ec0bcfe41bb`  
		Last Modified: Thu, 17 Oct 2024 09:14:36 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3.2` - unknown; unknown

```console
$ docker pull emqx@sha256:cf01109bace3c05412f2e4dacc0de4c71941a82f3e6f1560f6ca543bb7055d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2830199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0026944e55c7139e6d592d06ee03b4220fbcf76f54927a0b7ab8929e35a1d106`

```dockerfile
```

-	Layers:
	-	`sha256:5603f89b568936a407db00a85ddc384456fc1313821d4152ddc2fbb0906f7d6c`  
		Last Modified: Thu, 17 Oct 2024 09:14:37 GMT  
		Size: 2.8 MB (2817529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b75ba5d13d9fdf7caa9a00b851a4de2fef7f188cc600e141d96ce6ea8e3b744a`  
		Last Modified: Thu, 17 Oct 2024 09:14:36 GMT  
		Size: 12.7 KB (12670 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.4`

```console
$ docker pull emqx@sha256:0b9201a89764cddd3afc1f6ce8f5379935380deb7093e9e8d7be0007aed1094c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.4` - linux; amd64

```console
$ docker pull emqx@sha256:276456cb51108b2e019f048714e276e9eda8da1a1cf6e8de5dbc85a8219f220b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118702943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445f3e64be7e767a6b9383ec576cd093779ab4b37efd0aef3b27dc4b8daa3dfe`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902b9056c3f407fb651df741ab321c26dffbc2b0583e30626f04a5345b350cc2`  
		Last Modified: Thu, 17 Oct 2024 01:16:41 GMT  
		Size: 87.3 MB (87273212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec10531a42c5b130787f3f1c4365acae5459b64168b5ba2329525f6ab435f10`  
		Last Modified: Thu, 17 Oct 2024 01:16:40 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4` - unknown; unknown

```console
$ docker pull emqx@sha256:206dae2ca6bec5e9b7cad5032f1f92daa07a268280af9a7bbdb6ec1571f21f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c525ca519e2d03704c16db958e843a81e9e54b3c6f596df74f0a4df08467d9e2`

```dockerfile
```

-	Layers:
	-	`sha256:39b521bfbc3953a46182b620fce0db4934f44905787bbd723f79974d6495e49e`  
		Last Modified: Thu, 17 Oct 2024 01:16:40 GMT  
		Size: 2.8 MB (2810619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55cfc11100162b28f6d4360dccbaba10a3752880dc8fd6ba0f7376838155cbd6`  
		Last Modified: Thu, 17 Oct 2024 01:16:40 GMT  
		Size: 12.5 KB (12541 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:630f54dcf4abe45121044a97424ee7514f4d6df6885bfb215caa0f7a3bbcb369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108485671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bbd4295f65e5f11c0e90108287e02de9f088187c0567399ee12940dc42432b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196f527649c26b9c09daa1f29083267dea7de7faa1cfe6767c22ddf8581be857`  
		Last Modified: Thu, 17 Oct 2024 09:15:15 GMT  
		Size: 78.4 MB (78408982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9402679a386b02985738f56a0dcdc1fe9c5febae91918392cee2c70da4b87bf`  
		Last Modified: Thu, 17 Oct 2024 09:15:13 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4` - unknown; unknown

```console
$ docker pull emqx@sha256:abdbbac43feea2daeb194039c2aa3ae2530339e4659551f217b6e306b40b74fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc8d6fef451fafd44ee4088d05d993616ea0777e666ecd1e3b5f6a12c7cc20d`

```dockerfile
```

-	Layers:
	-	`sha256:a20288260e0aa92f13406757f49d772ab37ccf70b6ba730056809b2b1ca20805`  
		Last Modified: Thu, 17 Oct 2024 09:15:13 GMT  
		Size: 2.8 MB (2810854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f895eccf70b5a765a3881c214e837ec412277b4d672e86998c206b782988752`  
		Last Modified: Thu, 17 Oct 2024 09:15:13 GMT  
		Size: 12.6 KB (12615 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.4.1`

```console
$ docker pull emqx@sha256:0b9201a89764cddd3afc1f6ce8f5379935380deb7093e9e8d7be0007aed1094c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.4.1` - linux; amd64

```console
$ docker pull emqx@sha256:276456cb51108b2e019f048714e276e9eda8da1a1cf6e8de5dbc85a8219f220b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118702943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445f3e64be7e767a6b9383ec576cd093779ab4b37efd0aef3b27dc4b8daa3dfe`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902b9056c3f407fb651df741ab321c26dffbc2b0583e30626f04a5345b350cc2`  
		Last Modified: Thu, 17 Oct 2024 01:16:41 GMT  
		Size: 87.3 MB (87273212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec10531a42c5b130787f3f1c4365acae5459b64168b5ba2329525f6ab435f10`  
		Last Modified: Thu, 17 Oct 2024 01:16:40 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4.1` - unknown; unknown

```console
$ docker pull emqx@sha256:206dae2ca6bec5e9b7cad5032f1f92daa07a268280af9a7bbdb6ec1571f21f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c525ca519e2d03704c16db958e843a81e9e54b3c6f596df74f0a4df08467d9e2`

```dockerfile
```

-	Layers:
	-	`sha256:39b521bfbc3953a46182b620fce0db4934f44905787bbd723f79974d6495e49e`  
		Last Modified: Thu, 17 Oct 2024 01:16:40 GMT  
		Size: 2.8 MB (2810619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55cfc11100162b28f6d4360dccbaba10a3752880dc8fd6ba0f7376838155cbd6`  
		Last Modified: Thu, 17 Oct 2024 01:16:40 GMT  
		Size: 12.5 KB (12541 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.4.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:630f54dcf4abe45121044a97424ee7514f4d6df6885bfb215caa0f7a3bbcb369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108485671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bbd4295f65e5f11c0e90108287e02de9f088187c0567399ee12940dc42432b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196f527649c26b9c09daa1f29083267dea7de7faa1cfe6767c22ddf8581be857`  
		Last Modified: Thu, 17 Oct 2024 09:15:15 GMT  
		Size: 78.4 MB (78408982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9402679a386b02985738f56a0dcdc1fe9c5febae91918392cee2c70da4b87bf`  
		Last Modified: Thu, 17 Oct 2024 09:15:13 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4.1` - unknown; unknown

```console
$ docker pull emqx@sha256:abdbbac43feea2daeb194039c2aa3ae2530339e4659551f217b6e306b40b74fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc8d6fef451fafd44ee4088d05d993616ea0777e666ecd1e3b5f6a12c7cc20d`

```dockerfile
```

-	Layers:
	-	`sha256:a20288260e0aa92f13406757f49d772ab37ccf70b6ba730056809b2b1ca20805`  
		Last Modified: Thu, 17 Oct 2024 09:15:13 GMT  
		Size: 2.8 MB (2810854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f895eccf70b5a765a3881c214e837ec412277b4d672e86998c206b782988752`  
		Last Modified: Thu, 17 Oct 2024 09:15:13 GMT  
		Size: 12.6 KB (12615 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.5`

```console
$ docker pull emqx@sha256:bcd0f6a433ad0801b8ffc0b90a8a89370d6c6a27641dd47091e6d86e83d820d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.5` - linux; amd64

```console
$ docker pull emqx@sha256:f3990e288f51dc45b56f952cc1b46fbec198cca6c8ea0648ad4555575e6ab846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121269095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea8636d97dcc2e476f00f7bc0f092c9ecbfe5b201b7718919e04a86637c733c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc609b9ffc7494473374a74bae482c0072e6e9893d3ef8d4cb9141212131fd45`  
		Last Modified: Thu, 17 Oct 2024 01:16:32 GMT  
		Size: 89.8 MB (89839232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a8660c640b38e3779417c2a07bacd8f9c625449aa6bd5807942e842b5e7716`  
		Last Modified: Thu, 17 Oct 2024 01:16:31 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5` - unknown; unknown

```console
$ docker pull emqx@sha256:6f31337d285c9e4b7a25236bea9938232d36e075b5306fcd4e384cadc636a477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6cb611d9ea9447121783e57eb4554f437fae891d282cbf52f7acd9d15099852`

```dockerfile
```

-	Layers:
	-	`sha256:9bf1f67b2db71752aed25f7411ae59ff8504a8093c9c581d01fa9545823fc1b1`  
		Last Modified: Thu, 17 Oct 2024 01:16:31 GMT  
		Size: 2.8 MB (2810580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f75a85565d8bf0929b9b8d6974ea5c5599f346277f569512d882e064a1c715c`  
		Last Modified: Thu, 17 Oct 2024 01:16:31 GMT  
		Size: 12.6 KB (12643 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8d9a6a1a376e46727634c31f6a2fc3f2a8c8ee1a23f5e399abaf8da4cbe45f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116783858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571c88822fbc7ecb61de76f81ae5bb3bd58e60eed24960d0e99d12381cf8f3ac`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7242e4b2c3a003fe471d121bafc0effb9fc76218d570aa06f0e85ce9a59f8c`  
		Last Modified: Thu, 17 Oct 2024 09:15:59 GMT  
		Size: 86.7 MB (86707037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2c64bb0c14f7f6a9c21f26ee66642c402a88e6018ccd01a682a0d9e458d429`  
		Last Modified: Thu, 17 Oct 2024 09:15:57 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5` - unknown; unknown

```console
$ docker pull emqx@sha256:6ab120d1aaa4e8d7a30386eaa53db7b9fc714f1645feb289acb443a3cba37ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8c382fa440bae55c88830ced6eab6a1502be628da34a014a63f0346f4bf433`

```dockerfile
```

-	Layers:
	-	`sha256:71062cddcc04f2b48e59d820d69fb770947f25394c5e37cec74ec73445c64877`  
		Last Modified: Thu, 17 Oct 2024 09:15:57 GMT  
		Size: 2.8 MB (2810815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4b938a75b693aa93f706a690a2ebbbc0f9d2e921f3375798ef26cc85c00483c`  
		Last Modified: Thu, 17 Oct 2024 09:15:57 GMT  
		Size: 12.7 KB (12717 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.5.1`

```console
$ docker pull emqx@sha256:bcd0f6a433ad0801b8ffc0b90a8a89370d6c6a27641dd47091e6d86e83d820d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.5.1` - linux; amd64

```console
$ docker pull emqx@sha256:f3990e288f51dc45b56f952cc1b46fbec198cca6c8ea0648ad4555575e6ab846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121269095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea8636d97dcc2e476f00f7bc0f092c9ecbfe5b201b7718919e04a86637c733c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc609b9ffc7494473374a74bae482c0072e6e9893d3ef8d4cb9141212131fd45`  
		Last Modified: Thu, 17 Oct 2024 01:16:32 GMT  
		Size: 89.8 MB (89839232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a8660c640b38e3779417c2a07bacd8f9c625449aa6bd5807942e842b5e7716`  
		Last Modified: Thu, 17 Oct 2024 01:16:31 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:6f31337d285c9e4b7a25236bea9938232d36e075b5306fcd4e384cadc636a477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6cb611d9ea9447121783e57eb4554f437fae891d282cbf52f7acd9d15099852`

```dockerfile
```

-	Layers:
	-	`sha256:9bf1f67b2db71752aed25f7411ae59ff8504a8093c9c581d01fa9545823fc1b1`  
		Last Modified: Thu, 17 Oct 2024 01:16:31 GMT  
		Size: 2.8 MB (2810580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f75a85565d8bf0929b9b8d6974ea5c5599f346277f569512d882e064a1c715c`  
		Last Modified: Thu, 17 Oct 2024 01:16:31 GMT  
		Size: 12.6 KB (12643 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8d9a6a1a376e46727634c31f6a2fc3f2a8c8ee1a23f5e399abaf8da4cbe45f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116783858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571c88822fbc7ecb61de76f81ae5bb3bd58e60eed24960d0e99d12381cf8f3ac`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7242e4b2c3a003fe471d121bafc0effb9fc76218d570aa06f0e85ce9a59f8c`  
		Last Modified: Thu, 17 Oct 2024 09:15:59 GMT  
		Size: 86.7 MB (86707037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2c64bb0c14f7f6a9c21f26ee66642c402a88e6018ccd01a682a0d9e458d429`  
		Last Modified: Thu, 17 Oct 2024 09:15:57 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:6ab120d1aaa4e8d7a30386eaa53db7b9fc714f1645feb289acb443a3cba37ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8c382fa440bae55c88830ced6eab6a1502be628da34a014a63f0346f4bf433`

```dockerfile
```

-	Layers:
	-	`sha256:71062cddcc04f2b48e59d820d69fb770947f25394c5e37cec74ec73445c64877`  
		Last Modified: Thu, 17 Oct 2024 09:15:57 GMT  
		Size: 2.8 MB (2810815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4b938a75b693aa93f706a690a2ebbbc0f9d2e921f3375798ef26cc85c00483c`  
		Last Modified: Thu, 17 Oct 2024 09:15:57 GMT  
		Size: 12.7 KB (12717 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.6`

```console
$ docker pull emqx@sha256:df2cd99927c568da813cfc10643164ce8291ed93981cb677c7027edf03fc939f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.6` - linux; amd64

```console
$ docker pull emqx@sha256:9d082d824243004cc0427a47cc9a27d86f2ce0e5663656c2fda00ed933a450b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124182197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c183917b31b37977c0d0d6fef443a19107acf007cf4af2360467f5f7e13d31c0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdb51dd66dac85cff7f0dea12ae4cf2562d67b64f58356026d75267b51e7ddf`  
		Last Modified: Thu, 17 Oct 2024 01:16:52 GMT  
		Size: 95.1 MB (95054846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9223eda1dfe7a288d5cc6d8f10e890c8a83097afceec13ccfc239fa5ffd100e`  
		Last Modified: Thu, 17 Oct 2024 01:16:49 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6` - unknown; unknown

```console
$ docker pull emqx@sha256:a0bdccbf2dd2345089bf4c114bd5005fbc42d926030bc40d4b5c7f375989699b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c49136223e850624eaee8d9d4ab231053263b651f7a23a5d229e1b37a2fc447`

```dockerfile
```

-	Layers:
	-	`sha256:bb2d2db950d00939729d6fd98b9765a3774ea5a81a7e57604abb238568f7a54b`  
		Last Modified: Thu, 17 Oct 2024 01:16:50 GMT  
		Size: 2.6 MB (2591438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3856c759bd5c7534b61cb7f64116201cf7314c8fc651959658969f2ce4fd5880`  
		Last Modified: Thu, 17 Oct 2024 01:16:49 GMT  
		Size: 11.8 KB (11764 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:92d4b7c09c175b7d42b4b28cf8b6626c827adec0951d8c8d16b33296f701dfa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120776793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713b59c07160774d6329329475f338acbf94099f3b6d1262f7a9d87d97ea2702`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda3e30a054313d3e1439ad1ffcb0bb793be560b80a4ab846c7ab0ec1b825f2a`  
		Last Modified: Thu, 17 Oct 2024 09:16:45 GMT  
		Size: 91.6 MB (91619389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3384059eb918167c979a95ca94c0e772b38e6b7817b35b3816717797e15d4d3`  
		Last Modified: Thu, 17 Oct 2024 09:16:42 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6` - unknown; unknown

```console
$ docker pull emqx@sha256:645141760519b8e13cd57790596d1baaf3c0be9e63ad982d7d1387ef08b31a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0aa4b2904ac7240a55a910e2f130b375af48e11fc6e393ed71b1e6aec1b92b9`

```dockerfile
```

-	Layers:
	-	`sha256:7fa1fc0e0bebadc5526b60ffc558cab0af0f99d04cefc73b1be08896af518175`  
		Last Modified: Thu, 17 Oct 2024 09:16:43 GMT  
		Size: 2.6 MB (2591693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f4abee03b88459aea7d151d348b32706da0255350917316de471c6d69fd7a0`  
		Last Modified: Thu, 17 Oct 2024 09:16:42 GMT  
		Size: 11.8 KB (11839 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.6.1`

```console
$ docker pull emqx@sha256:df2cd99927c568da813cfc10643164ce8291ed93981cb677c7027edf03fc939f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.6.1` - linux; amd64

```console
$ docker pull emqx@sha256:9d082d824243004cc0427a47cc9a27d86f2ce0e5663656c2fda00ed933a450b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124182197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c183917b31b37977c0d0d6fef443a19107acf007cf4af2360467f5f7e13d31c0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdb51dd66dac85cff7f0dea12ae4cf2562d67b64f58356026d75267b51e7ddf`  
		Last Modified: Thu, 17 Oct 2024 01:16:52 GMT  
		Size: 95.1 MB (95054846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9223eda1dfe7a288d5cc6d8f10e890c8a83097afceec13ccfc239fa5ffd100e`  
		Last Modified: Thu, 17 Oct 2024 01:16:49 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6.1` - unknown; unknown

```console
$ docker pull emqx@sha256:a0bdccbf2dd2345089bf4c114bd5005fbc42d926030bc40d4b5c7f375989699b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c49136223e850624eaee8d9d4ab231053263b651f7a23a5d229e1b37a2fc447`

```dockerfile
```

-	Layers:
	-	`sha256:bb2d2db950d00939729d6fd98b9765a3774ea5a81a7e57604abb238568f7a54b`  
		Last Modified: Thu, 17 Oct 2024 01:16:50 GMT  
		Size: 2.6 MB (2591438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3856c759bd5c7534b61cb7f64116201cf7314c8fc651959658969f2ce4fd5880`  
		Last Modified: Thu, 17 Oct 2024 01:16:49 GMT  
		Size: 11.8 KB (11764 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.6.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:92d4b7c09c175b7d42b4b28cf8b6626c827adec0951d8c8d16b33296f701dfa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120776793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713b59c07160774d6329329475f338acbf94099f3b6d1262f7a9d87d97ea2702`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda3e30a054313d3e1439ad1ffcb0bb793be560b80a4ab846c7ab0ec1b825f2a`  
		Last Modified: Thu, 17 Oct 2024 09:16:45 GMT  
		Size: 91.6 MB (91619389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3384059eb918167c979a95ca94c0e772b38e6b7817b35b3816717797e15d4d3`  
		Last Modified: Thu, 17 Oct 2024 09:16:42 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6.1` - unknown; unknown

```console
$ docker pull emqx@sha256:645141760519b8e13cd57790596d1baaf3c0be9e63ad982d7d1387ef08b31a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0aa4b2904ac7240a55a910e2f130b375af48e11fc6e393ed71b1e6aec1b92b9`

```dockerfile
```

-	Layers:
	-	`sha256:7fa1fc0e0bebadc5526b60ffc558cab0af0f99d04cefc73b1be08896af518175`  
		Last Modified: Thu, 17 Oct 2024 09:16:43 GMT  
		Size: 2.6 MB (2591693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f4abee03b88459aea7d151d348b32706da0255350917316de471c6d69fd7a0`  
		Last Modified: Thu, 17 Oct 2024 09:16:42 GMT  
		Size: 11.8 KB (11839 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:423bf64910d27fcbd0e5483de4b264449d9c690906dcaedf48e5c2626cefabeb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:ef072cd8af4f3387f128aa25c200120f0f208ff073a5d27579c3716e2860bffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126274509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe4f8022735b2a0947117d09dbe0d924879b3a75d3a70ec18cb51ea6c955747`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["bash"]
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd879c6d847eda7a45ec51dafe5f734ffa9bcd3747043d31ab1e60816b6da5f`  
		Last Modified: Thu, 17 Oct 2024 01:16:53 GMT  
		Size: 97.1 MB (97147158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f3f29eb40c72dc616939f5fae785094eaf40bbc4578b1cd350a78d62a124e7`  
		Last Modified: Thu, 17 Oct 2024 01:16:51 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:0fcddb44abf10dd6e71f05e625baaa8fb4411aad2984c78d8c79104d02da8fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2610957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37be108f58213bfbd39c62691be88e12895ad0c00ca33df33f2a3a5ce09ad10e`

```dockerfile
```

-	Layers:
	-	`sha256:b1ced7a713d00397f1ed14ef32f01456684b39432b4199e3da14ba45192113f5`  
		Last Modified: Thu, 17 Oct 2024 01:16:51 GMT  
		Size: 2.6 MB (2599192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d55b14480f69e2bd2ddab3b77baa74851de9e5f8c3a982626929d0a12a56f20`  
		Last Modified: Thu, 17 Oct 2024 01:16:51 GMT  
		Size: 11.8 KB (11765 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:1e023042ab94c46f63e8ba10ee79831755e9deea0ec7969f5abc59ae5af23dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122852480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3738fa0f56725034647484875df9d8f898c6f575631ae79f6094834f4b842eee`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["bash"]
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4754fd85bd5726e504564981e0a7bfc71d5095b51fd1f0ff348b4757b68b9912`  
		Last Modified: Thu, 17 Oct 2024 09:17:29 GMT  
		Size: 93.7 MB (93695076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690e48249e1ea1d83400c3e0019e1558e0a004a2435395d285cfa4ec73e41cf5`  
		Last Modified: Thu, 17 Oct 2024 09:17:26 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:67aa91f089245d9d35ddf399d3dcfa1b05e9a81f0f6b43cb3bd4227e41af0568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2611286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3c45fe27c5adfaf6f165b2138479071e504cd70ecac8c4c307ad000213e390`

```dockerfile
```

-	Layers:
	-	`sha256:db1493ff1a22a112454505e5ffb5415165ddcfc2beb9c3842a6162d940cb1d50`  
		Last Modified: Thu, 17 Oct 2024 09:17:26 GMT  
		Size: 2.6 MB (2599447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:164215e08ee5d792efae718576461cc58428f0e8214fdf9eac80b5b7c0bc9f7b`  
		Last Modified: Thu, 17 Oct 2024 09:17:26 GMT  
		Size: 11.8 KB (11839 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:423bf64910d27fcbd0e5483de4b264449d9c690906dcaedf48e5c2626cefabeb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:ef072cd8af4f3387f128aa25c200120f0f208ff073a5d27579c3716e2860bffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126274509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe4f8022735b2a0947117d09dbe0d924879b3a75d3a70ec18cb51ea6c955747`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["bash"]
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd879c6d847eda7a45ec51dafe5f734ffa9bcd3747043d31ab1e60816b6da5f`  
		Last Modified: Thu, 17 Oct 2024 01:16:53 GMT  
		Size: 97.1 MB (97147158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f3f29eb40c72dc616939f5fae785094eaf40bbc4578b1cd350a78d62a124e7`  
		Last Modified: Thu, 17 Oct 2024 01:16:51 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:0fcddb44abf10dd6e71f05e625baaa8fb4411aad2984c78d8c79104d02da8fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2610957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37be108f58213bfbd39c62691be88e12895ad0c00ca33df33f2a3a5ce09ad10e`

```dockerfile
```

-	Layers:
	-	`sha256:b1ced7a713d00397f1ed14ef32f01456684b39432b4199e3da14ba45192113f5`  
		Last Modified: Thu, 17 Oct 2024 01:16:51 GMT  
		Size: 2.6 MB (2599192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d55b14480f69e2bd2ddab3b77baa74851de9e5f8c3a982626929d0a12a56f20`  
		Last Modified: Thu, 17 Oct 2024 01:16:51 GMT  
		Size: 11.8 KB (11765 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:1e023042ab94c46f63e8ba10ee79831755e9deea0ec7969f5abc59ae5af23dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122852480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3738fa0f56725034647484875df9d8f898c6f575631ae79f6094834f4b842eee`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["bash"]
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4754fd85bd5726e504564981e0a7bfc71d5095b51fd1f0ff348b4757b68b9912`  
		Last Modified: Thu, 17 Oct 2024 09:17:29 GMT  
		Size: 93.7 MB (93695076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690e48249e1ea1d83400c3e0019e1558e0a004a2435395d285cfa4ec73e41cf5`  
		Last Modified: Thu, 17 Oct 2024 09:17:26 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:67aa91f089245d9d35ddf399d3dcfa1b05e9a81f0f6b43cb3bd4227e41af0568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2611286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3c45fe27c5adfaf6f165b2138479071e504cd70ecac8c4c307ad000213e390`

```dockerfile
```

-	Layers:
	-	`sha256:db1493ff1a22a112454505e5ffb5415165ddcfc2beb9c3842a6162d940cb1d50`  
		Last Modified: Thu, 17 Oct 2024 09:17:26 GMT  
		Size: 2.6 MB (2599447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:164215e08ee5d792efae718576461cc58428f0e8214fdf9eac80b5b7c0bc9f7b`  
		Last Modified: Thu, 17 Oct 2024 09:17:26 GMT  
		Size: 11.8 KB (11839 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:983d885bc1b76818bb769b1a1f4b8d713e7284e3ba72f931dc622cb4f97bfcfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:73f08b2ec0fb38e8c6b5222d2031058f92bae434e7781710f66f23f3de5dd2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109909273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c07a2f6f89b0a41ceb960016e53260246391c1ab3809ea8b1bf34e5e8f79310`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9001c341bcd760753ca192f57aac4c3ca6fe825b997840e0c18c72be1918b846`  
		Last Modified: Tue, 22 Oct 2024 16:56:08 GMT  
		Size: 80.8 MB (80781921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6d3bf26a86d0be8a04317b104743cef6703e83474b5dce305c1224feb82b4a`  
		Last Modified: Tue, 22 Oct 2024 16:56:06 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:2825e8d0751787152a7b58a9df04c82cdb4ee14e63a0b6a66b84490578ec6523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e15900551528293de41105bd08e012a64b57684f45c442d67b625e48a6dc4b8`

```dockerfile
```

-	Layers:
	-	`sha256:dcc3d0d5953a5fcf16da7dcada7a76eb83a75caf0345a35b14ba0a91978afb0f`  
		Last Modified: Tue, 22 Oct 2024 16:56:06 GMT  
		Size: 2.6 MB (2624750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb19138927642c0126a5d50f64367e4fc24e72878dde16f28c07a091b1d2a8f7`  
		Last Modified: Tue, 22 Oct 2024 16:56:06 GMT  
		Size: 12.3 KB (12315 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:bf84a3fdb8b744f65cc83b078fe6f6bbc09eac84de5c2c2d257cee6d0b2b65fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107097129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32632f41a7369effd68aa93f80c8a37c96bc903fe868f0e38de6fb9e2fba076d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d196bcfe1e1b9d831f9206be1909867be476ebcc4cd14abf81cc717c29d7274a`  
		Last Modified: Tue, 22 Oct 2024 16:55:57 GMT  
		Size: 77.9 MB (77939724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c5321e15b65b59f02dfcb34cd289b3fff03c36a88b952fb2dcb95a257a524d`  
		Last Modified: Tue, 22 Oct 2024 16:55:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:285fbd3d644a00c7a1e9426c8ecbb2642f5dc8752c49f7a06099b11cdbd9012a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84222ce87ed3bdeb1128239b1854b6149b40427373de46897280f30b997cc808`

```dockerfile
```

-	Layers:
	-	`sha256:a06dcdbccb3564a9fde3d56f720598ebc16df41eb292bbc083e813bdf7c8b299`  
		Last Modified: Tue, 22 Oct 2024 16:55:55 GMT  
		Size: 2.6 MB (2625029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bccbfcfd1900f2bab668677abbdc31bd269ea5c79d3d821c6bccc538d669d6bd`  
		Last Modified: Tue, 22 Oct 2024 16:55:55 GMT  
		Size: 12.4 KB (12437 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.1`

```console
$ docker pull emqx@sha256:983d885bc1b76818bb769b1a1f4b8d713e7284e3ba72f931dc622cb4f97bfcfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.1` - linux; amd64

```console
$ docker pull emqx@sha256:73f08b2ec0fb38e8c6b5222d2031058f92bae434e7781710f66f23f3de5dd2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109909273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c07a2f6f89b0a41ceb960016e53260246391c1ab3809ea8b1bf34e5e8f79310`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9001c341bcd760753ca192f57aac4c3ca6fe825b997840e0c18c72be1918b846`  
		Last Modified: Tue, 22 Oct 2024 16:56:08 GMT  
		Size: 80.8 MB (80781921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6d3bf26a86d0be8a04317b104743cef6703e83474b5dce305c1224feb82b4a`  
		Last Modified: Tue, 22 Oct 2024 16:56:06 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.1` - unknown; unknown

```console
$ docker pull emqx@sha256:2825e8d0751787152a7b58a9df04c82cdb4ee14e63a0b6a66b84490578ec6523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e15900551528293de41105bd08e012a64b57684f45c442d67b625e48a6dc4b8`

```dockerfile
```

-	Layers:
	-	`sha256:dcc3d0d5953a5fcf16da7dcada7a76eb83a75caf0345a35b14ba0a91978afb0f`  
		Last Modified: Tue, 22 Oct 2024 16:56:06 GMT  
		Size: 2.6 MB (2624750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb19138927642c0126a5d50f64367e4fc24e72878dde16f28c07a091b1d2a8f7`  
		Last Modified: Tue, 22 Oct 2024 16:56:06 GMT  
		Size: 12.3 KB (12315 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:bf84a3fdb8b744f65cc83b078fe6f6bbc09eac84de5c2c2d257cee6d0b2b65fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107097129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32632f41a7369effd68aa93f80c8a37c96bc903fe868f0e38de6fb9e2fba076d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d196bcfe1e1b9d831f9206be1909867be476ebcc4cd14abf81cc717c29d7274a`  
		Last Modified: Tue, 22 Oct 2024 16:55:57 GMT  
		Size: 77.9 MB (77939724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c5321e15b65b59f02dfcb34cd289b3fff03c36a88b952fb2dcb95a257a524d`  
		Last Modified: Tue, 22 Oct 2024 16:55:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.1` - unknown; unknown

```console
$ docker pull emqx@sha256:285fbd3d644a00c7a1e9426c8ecbb2642f5dc8752c49f7a06099b11cdbd9012a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84222ce87ed3bdeb1128239b1854b6149b40427373de46897280f30b997cc808`

```dockerfile
```

-	Layers:
	-	`sha256:a06dcdbccb3564a9fde3d56f720598ebc16df41eb292bbc083e813bdf7c8b299`  
		Last Modified: Tue, 22 Oct 2024 16:55:55 GMT  
		Size: 2.6 MB (2625029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bccbfcfd1900f2bab668677abbdc31bd269ea5c79d3d821c6bccc538d669d6bd`  
		Last Modified: Tue, 22 Oct 2024 16:55:55 GMT  
		Size: 12.4 KB (12437 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:983d885bc1b76818bb769b1a1f4b8d713e7284e3ba72f931dc622cb4f97bfcfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:73f08b2ec0fb38e8c6b5222d2031058f92bae434e7781710f66f23f3de5dd2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109909273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c07a2f6f89b0a41ceb960016e53260246391c1ab3809ea8b1bf34e5e8f79310`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9001c341bcd760753ca192f57aac4c3ca6fe825b997840e0c18c72be1918b846`  
		Last Modified: Tue, 22 Oct 2024 16:56:08 GMT  
		Size: 80.8 MB (80781921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6d3bf26a86d0be8a04317b104743cef6703e83474b5dce305c1224feb82b4a`  
		Last Modified: Tue, 22 Oct 2024 16:56:06 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:2825e8d0751787152a7b58a9df04c82cdb4ee14e63a0b6a66b84490578ec6523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e15900551528293de41105bd08e012a64b57684f45c442d67b625e48a6dc4b8`

```dockerfile
```

-	Layers:
	-	`sha256:dcc3d0d5953a5fcf16da7dcada7a76eb83a75caf0345a35b14ba0a91978afb0f`  
		Last Modified: Tue, 22 Oct 2024 16:56:06 GMT  
		Size: 2.6 MB (2624750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb19138927642c0126a5d50f64367e4fc24e72878dde16f28c07a091b1d2a8f7`  
		Last Modified: Tue, 22 Oct 2024 16:56:06 GMT  
		Size: 12.3 KB (12315 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:bf84a3fdb8b744f65cc83b078fe6f6bbc09eac84de5c2c2d257cee6d0b2b65fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107097129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32632f41a7369effd68aa93f80c8a37c96bc903fe868f0e38de6fb9e2fba076d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d196bcfe1e1b9d831f9206be1909867be476ebcc4cd14abf81cc717c29d7274a`  
		Last Modified: Tue, 22 Oct 2024 16:55:57 GMT  
		Size: 77.9 MB (77939724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c5321e15b65b59f02dfcb34cd289b3fff03c36a88b952fb2dcb95a257a524d`  
		Last Modified: Tue, 22 Oct 2024 16:55:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:285fbd3d644a00c7a1e9426c8ecbb2642f5dc8752c49f7a06099b11cdbd9012a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84222ce87ed3bdeb1128239b1854b6149b40427373de46897280f30b997cc808`

```dockerfile
```

-	Layers:
	-	`sha256:a06dcdbccb3564a9fde3d56f720598ebc16df41eb292bbc083e813bdf7c8b299`  
		Last Modified: Tue, 22 Oct 2024 16:55:55 GMT  
		Size: 2.6 MB (2625029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bccbfcfd1900f2bab668677abbdc31bd269ea5c79d3d821c6bccc538d669d6bd`  
		Last Modified: Tue, 22 Oct 2024 16:55:55 GMT  
		Size: 12.4 KB (12437 bytes)  
		MIME: application/vnd.in-toto+json
