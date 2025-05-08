<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.6`](#emqx586)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:78464a448a335f3cb82525499848a712f2453ae9cf8686f22da402706f29d72e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:8e9640f8fd8dcddf45b2b3f208e65efba5ad76f3b0516a83abe1812319b5bcca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105504221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a749249703327cbb17185e8cd68a4bbf0a55429bcdb75da7a6ee110641badf0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 25 Mar 2025 16:14:46 GMT
ENV EMQX_VERSION=5.8.6
# Tue, 25 Mar 2025 16:14:46 GMT
ENV AMD64_SHA256=430f69c24c0d659a9ce2e902d018c6dd20565519925e0cc893980d824b0a952e
# Tue, 25 Mar 2025 16:14:46 GMT
ENV ARM64_SHA256=dcabedb9d3888e0fb6e8138da6ae3d8ef1afce1f85e4580f26f19d65115ed5c3
# Tue, 25 Mar 2025 16:14:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 25 Mar 2025 16:14:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
WORKDIR /opt/emqx
# Tue, 25 Mar 2025 16:14:46 GMT
USER emqx
# Tue, 25 Mar 2025 16:14:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Mar 2025 16:14:46 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 25 Mar 2025 16:14:46 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 16:14:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07636c07c94e945b674445fd1c661d1107fc9dbf2bf0f8278215d255283e988`  
		Last Modified: Thu, 08 May 2025 17:24:28 GMT  
		Size: 77.3 MB (77275516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71f4f3a12090159d90e569c5161ed3c56c0458ec151718bfcf49bff73b930c2`  
		Last Modified: Thu, 08 May 2025 17:24:11 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:caff0cb09d946e6afab72667346f01a6fc2004b501d06c5fca9ae4b22a8f2b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ba7e3aa0d0f1ce3b7303677e2ead6d9618a402be77bf6549c6d4107217b158`

```dockerfile
```

-	Layers:
	-	`sha256:bfd76372ba86fbfd83f15b70c440f679d43e49b33e0eae9ea12b8f5a35e9513a`  
		Last Modified: Mon, 28 Apr 2025 21:42:18 GMT  
		Size: 2.6 MB (2615858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c1ebf69ed8a1872a88ed717829801ff4f307032890669ebe6f54c23e8e2295`  
		Last Modified: Mon, 28 Apr 2025 21:42:17 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:ff0e514dcb5d97d34836fb0f3557e43fc7187866798d41ffb9a74df562cc5630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102617680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764d92b8fe48d4d1237b48ef9b19282c9a28b682ed679aac129666529041b360`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 25 Mar 2025 16:14:46 GMT
ENV EMQX_VERSION=5.8.6
# Tue, 25 Mar 2025 16:14:46 GMT
ENV AMD64_SHA256=430f69c24c0d659a9ce2e902d018c6dd20565519925e0cc893980d824b0a952e
# Tue, 25 Mar 2025 16:14:46 GMT
ENV ARM64_SHA256=dcabedb9d3888e0fb6e8138da6ae3d8ef1afce1f85e4580f26f19d65115ed5c3
# Tue, 25 Mar 2025 16:14:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 25 Mar 2025 16:14:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
WORKDIR /opt/emqx
# Tue, 25 Mar 2025 16:14:46 GMT
USER emqx
# Tue, 25 Mar 2025 16:14:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Mar 2025 16:14:46 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 25 Mar 2025 16:14:46 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 16:14:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9407aa8b55deb4df74d0efe7e8b3f932d9b641efc8288fc8c66f2395d7efeb0b`  
		Last Modified: Thu, 08 May 2025 17:50:23 GMT  
		Size: 74.5 MB (74549996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f46b7da4817f32733b4919e3407cffec88d7835f7a9b46ccc58323abaf1163`  
		Last Modified: Thu, 08 May 2025 17:50:15 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:87b4132c9be52d9b48c8bdaf20edaca01c361d2987166cd80977e1f7cb86f3f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7858099c1efd8c3d562ecbe75873ad620019933de433168cdf92bb463d0f1ddc`

```dockerfile
```

-	Layers:
	-	`sha256:98e4fd22817af6e0c5ac88c6250e6332cbcb01f58e35639ae697b7c35f02fd54`  
		Last Modified: Mon, 28 Apr 2025 21:45:03 GMT  
		Size: 2.6 MB (2616138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16b11e87747e9af4e605b69f2e8b216d97192ebb98a146cf94c7e238e5d9e528`  
		Last Modified: Mon, 28 Apr 2025 21:45:02 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:521c380220604e8324c744f3cc28238f43a97d7612752a4489a376a9394533a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:d2ec9e1eea5829c2176ed8115ec1a95d5b92516f2905c1048126180cb66db2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125376734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd41bf1199c30f1b6c62f1c835de98c8bd86f77f47e6e3368d084f6a8a1dd384`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6384c1ae34ef5fe5e8f9c7d026cb212801ce94dae76d6cd0a4b137503ef1493c`  
		Last Modified: Mon, 28 Apr 2025 21:42:35 GMT  
		Size: 97.1 MB (97148030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef08ead818ef00757d335e5a6a9722753ae02ffc854acceabe8ed132785b754`  
		Last Modified: Mon, 28 Apr 2025 21:42:31 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:ec764758cfc982702bc745b15bf92495c65590bd0ffe6436f25b0aa7a48f7409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bb5ddc0a795f2abdab765c02234756aea5c3e4faf531cb478b22928bf3d025`

```dockerfile
```

-	Layers:
	-	`sha256:10cc1b76f187cf6ade061ef151cfc2ee0f305280897ca7415482818c6234ca18`  
		Last Modified: Mon, 28 Apr 2025 21:42:31 GMT  
		Size: 2.6 MB (2625251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a739e0a5b9f8bef62e7ddda70c2c0678ef552290e24f144d2cc6a2aa30bfaad1`  
		Last Modified: Mon, 28 Apr 2025 21:42:31 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:818abbd29e0d80e23b4aeadb78244f4302e7ceeacef14699ded099fb8936e939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121763528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5530bc450f0f1f980b5253252063ec35c76462da30a1d09edbe3d59f2ff9403b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aded1074e652fd0c927f3aa2ef904c4da8cb4221f409be5ef166ee0ece6965f`  
		Last Modified: Mon, 28 Apr 2025 21:44:35 GMT  
		Size: 93.7 MB (93695842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fed40654e6bbe634aecb6f7732db79217ab96c6b9b1864d95326295fbe1999f`  
		Last Modified: Mon, 28 Apr 2025 21:44:32 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:fb68e087eb03a064952e559ff299fb8b35a1d65a07acb102149474d000b59b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9e9dfc2d4a90ca6d10f03a9be59bb433d60aef7e6ecc519b905078cbb4ba27`

```dockerfile
```

-	Layers:
	-	`sha256:c1ad1d44d0eb9ebd7a966e7103070ec1f1809e73ed94a4c3b9ac1eff07098b60`  
		Last Modified: Mon, 28 Apr 2025 21:44:32 GMT  
		Size: 2.6 MB (2625507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc298c4b8140e48f0a9399b7d65cba2532e1e9e774b2e911cdf3415f5c358d94`  
		Last Modified: Mon, 28 Apr 2025 21:44:32 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:521c380220604e8324c744f3cc28238f43a97d7612752a4489a376a9394533a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:d2ec9e1eea5829c2176ed8115ec1a95d5b92516f2905c1048126180cb66db2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125376734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd41bf1199c30f1b6c62f1c835de98c8bd86f77f47e6e3368d084f6a8a1dd384`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6384c1ae34ef5fe5e8f9c7d026cb212801ce94dae76d6cd0a4b137503ef1493c`  
		Last Modified: Mon, 28 Apr 2025 21:42:35 GMT  
		Size: 97.1 MB (97148030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef08ead818ef00757d335e5a6a9722753ae02ffc854acceabe8ed132785b754`  
		Last Modified: Mon, 28 Apr 2025 21:42:31 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:ec764758cfc982702bc745b15bf92495c65590bd0ffe6436f25b0aa7a48f7409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bb5ddc0a795f2abdab765c02234756aea5c3e4faf531cb478b22928bf3d025`

```dockerfile
```

-	Layers:
	-	`sha256:10cc1b76f187cf6ade061ef151cfc2ee0f305280897ca7415482818c6234ca18`  
		Last Modified: Mon, 28 Apr 2025 21:42:31 GMT  
		Size: 2.6 MB (2625251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a739e0a5b9f8bef62e7ddda70c2c0678ef552290e24f144d2cc6a2aa30bfaad1`  
		Last Modified: Mon, 28 Apr 2025 21:42:31 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:818abbd29e0d80e23b4aeadb78244f4302e7ceeacef14699ded099fb8936e939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121763528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5530bc450f0f1f980b5253252063ec35c76462da30a1d09edbe3d59f2ff9403b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aded1074e652fd0c927f3aa2ef904c4da8cb4221f409be5ef166ee0ece6965f`  
		Last Modified: Mon, 28 Apr 2025 21:44:35 GMT  
		Size: 93.7 MB (93695842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fed40654e6bbe634aecb6f7732db79217ab96c6b9b1864d95326295fbe1999f`  
		Last Modified: Mon, 28 Apr 2025 21:44:32 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:fb68e087eb03a064952e559ff299fb8b35a1d65a07acb102149474d000b59b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9e9dfc2d4a90ca6d10f03a9be59bb433d60aef7e6ecc519b905078cbb4ba27`

```dockerfile
```

-	Layers:
	-	`sha256:c1ad1d44d0eb9ebd7a966e7103070ec1f1809e73ed94a4c3b9ac1eff07098b60`  
		Last Modified: Mon, 28 Apr 2025 21:44:32 GMT  
		Size: 2.6 MB (2625507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc298c4b8140e48f0a9399b7d65cba2532e1e9e774b2e911cdf3415f5c358d94`  
		Last Modified: Mon, 28 Apr 2025 21:44:32 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:78464a448a335f3cb82525499848a712f2453ae9cf8686f22da402706f29d72e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:8e9640f8fd8dcddf45b2b3f208e65efba5ad76f3b0516a83abe1812319b5bcca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105504221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a749249703327cbb17185e8cd68a4bbf0a55429bcdb75da7a6ee110641badf0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 25 Mar 2025 16:14:46 GMT
ENV EMQX_VERSION=5.8.6
# Tue, 25 Mar 2025 16:14:46 GMT
ENV AMD64_SHA256=430f69c24c0d659a9ce2e902d018c6dd20565519925e0cc893980d824b0a952e
# Tue, 25 Mar 2025 16:14:46 GMT
ENV ARM64_SHA256=dcabedb9d3888e0fb6e8138da6ae3d8ef1afce1f85e4580f26f19d65115ed5c3
# Tue, 25 Mar 2025 16:14:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 25 Mar 2025 16:14:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
WORKDIR /opt/emqx
# Tue, 25 Mar 2025 16:14:46 GMT
USER emqx
# Tue, 25 Mar 2025 16:14:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Mar 2025 16:14:46 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 25 Mar 2025 16:14:46 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 16:14:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07636c07c94e945b674445fd1c661d1107fc9dbf2bf0f8278215d255283e988`  
		Last Modified: Thu, 08 May 2025 17:24:28 GMT  
		Size: 77.3 MB (77275516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71f4f3a12090159d90e569c5161ed3c56c0458ec151718bfcf49bff73b930c2`  
		Last Modified: Thu, 08 May 2025 17:24:11 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:caff0cb09d946e6afab72667346f01a6fc2004b501d06c5fca9ae4b22a8f2b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ba7e3aa0d0f1ce3b7303677e2ead6d9618a402be77bf6549c6d4107217b158`

```dockerfile
```

-	Layers:
	-	`sha256:bfd76372ba86fbfd83f15b70c440f679d43e49b33e0eae9ea12b8f5a35e9513a`  
		Last Modified: Mon, 28 Apr 2025 21:42:18 GMT  
		Size: 2.6 MB (2615858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c1ebf69ed8a1872a88ed717829801ff4f307032890669ebe6f54c23e8e2295`  
		Last Modified: Mon, 28 Apr 2025 21:42:17 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:ff0e514dcb5d97d34836fb0f3557e43fc7187866798d41ffb9a74df562cc5630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102617680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764d92b8fe48d4d1237b48ef9b19282c9a28b682ed679aac129666529041b360`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 25 Mar 2025 16:14:46 GMT
ENV EMQX_VERSION=5.8.6
# Tue, 25 Mar 2025 16:14:46 GMT
ENV AMD64_SHA256=430f69c24c0d659a9ce2e902d018c6dd20565519925e0cc893980d824b0a952e
# Tue, 25 Mar 2025 16:14:46 GMT
ENV ARM64_SHA256=dcabedb9d3888e0fb6e8138da6ae3d8ef1afce1f85e4580f26f19d65115ed5c3
# Tue, 25 Mar 2025 16:14:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 25 Mar 2025 16:14:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
WORKDIR /opt/emqx
# Tue, 25 Mar 2025 16:14:46 GMT
USER emqx
# Tue, 25 Mar 2025 16:14:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Mar 2025 16:14:46 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 25 Mar 2025 16:14:46 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 16:14:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9407aa8b55deb4df74d0efe7e8b3f932d9b641efc8288fc8c66f2395d7efeb0b`  
		Last Modified: Thu, 08 May 2025 17:50:23 GMT  
		Size: 74.5 MB (74549996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f46b7da4817f32733b4919e3407cffec88d7835f7a9b46ccc58323abaf1163`  
		Last Modified: Thu, 08 May 2025 17:50:15 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:87b4132c9be52d9b48c8bdaf20edaca01c361d2987166cd80977e1f7cb86f3f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7858099c1efd8c3d562ecbe75873ad620019933de433168cdf92bb463d0f1ddc`

```dockerfile
```

-	Layers:
	-	`sha256:98e4fd22817af6e0c5ac88c6250e6332cbcb01f58e35639ae697b7c35f02fd54`  
		Last Modified: Mon, 28 Apr 2025 21:45:03 GMT  
		Size: 2.6 MB (2616138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16b11e87747e9af4e605b69f2e8b216d97192ebb98a146cf94c7e238e5d9e528`  
		Last Modified: Mon, 28 Apr 2025 21:45:02 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.6`

```console
$ docker pull emqx@sha256:78464a448a335f3cb82525499848a712f2453ae9cf8686f22da402706f29d72e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.6` - linux; amd64

```console
$ docker pull emqx@sha256:8e9640f8fd8dcddf45b2b3f208e65efba5ad76f3b0516a83abe1812319b5bcca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105504221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a749249703327cbb17185e8cd68a4bbf0a55429bcdb75da7a6ee110641badf0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 25 Mar 2025 16:14:46 GMT
ENV EMQX_VERSION=5.8.6
# Tue, 25 Mar 2025 16:14:46 GMT
ENV AMD64_SHA256=430f69c24c0d659a9ce2e902d018c6dd20565519925e0cc893980d824b0a952e
# Tue, 25 Mar 2025 16:14:46 GMT
ENV ARM64_SHA256=dcabedb9d3888e0fb6e8138da6ae3d8ef1afce1f85e4580f26f19d65115ed5c3
# Tue, 25 Mar 2025 16:14:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 25 Mar 2025 16:14:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
WORKDIR /opt/emqx
# Tue, 25 Mar 2025 16:14:46 GMT
USER emqx
# Tue, 25 Mar 2025 16:14:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Mar 2025 16:14:46 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 25 Mar 2025 16:14:46 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 16:14:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07636c07c94e945b674445fd1c661d1107fc9dbf2bf0f8278215d255283e988`  
		Last Modified: Thu, 08 May 2025 17:24:28 GMT  
		Size: 77.3 MB (77275516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71f4f3a12090159d90e569c5161ed3c56c0458ec151718bfcf49bff73b930c2`  
		Last Modified: Thu, 08 May 2025 17:24:11 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.6` - unknown; unknown

```console
$ docker pull emqx@sha256:caff0cb09d946e6afab72667346f01a6fc2004b501d06c5fca9ae4b22a8f2b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ba7e3aa0d0f1ce3b7303677e2ead6d9618a402be77bf6549c6d4107217b158`

```dockerfile
```

-	Layers:
	-	`sha256:bfd76372ba86fbfd83f15b70c440f679d43e49b33e0eae9ea12b8f5a35e9513a`  
		Last Modified: Mon, 28 Apr 2025 21:42:18 GMT  
		Size: 2.6 MB (2615858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c1ebf69ed8a1872a88ed717829801ff4f307032890669ebe6f54c23e8e2295`  
		Last Modified: Mon, 28 Apr 2025 21:42:17 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:ff0e514dcb5d97d34836fb0f3557e43fc7187866798d41ffb9a74df562cc5630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102617680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764d92b8fe48d4d1237b48ef9b19282c9a28b682ed679aac129666529041b360`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 25 Mar 2025 16:14:46 GMT
ENV EMQX_VERSION=5.8.6
# Tue, 25 Mar 2025 16:14:46 GMT
ENV AMD64_SHA256=430f69c24c0d659a9ce2e902d018c6dd20565519925e0cc893980d824b0a952e
# Tue, 25 Mar 2025 16:14:46 GMT
ENV ARM64_SHA256=dcabedb9d3888e0fb6e8138da6ae3d8ef1afce1f85e4580f26f19d65115ed5c3
# Tue, 25 Mar 2025 16:14:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 25 Mar 2025 16:14:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
WORKDIR /opt/emqx
# Tue, 25 Mar 2025 16:14:46 GMT
USER emqx
# Tue, 25 Mar 2025 16:14:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Mar 2025 16:14:46 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 25 Mar 2025 16:14:46 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 16:14:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9407aa8b55deb4df74d0efe7e8b3f932d9b641efc8288fc8c66f2395d7efeb0b`  
		Last Modified: Thu, 08 May 2025 17:50:23 GMT  
		Size: 74.5 MB (74549996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f46b7da4817f32733b4919e3407cffec88d7835f7a9b46ccc58323abaf1163`  
		Last Modified: Thu, 08 May 2025 17:50:15 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.6` - unknown; unknown

```console
$ docker pull emqx@sha256:87b4132c9be52d9b48c8bdaf20edaca01c361d2987166cd80977e1f7cb86f3f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7858099c1efd8c3d562ecbe75873ad620019933de433168cdf92bb463d0f1ddc`

```dockerfile
```

-	Layers:
	-	`sha256:98e4fd22817af6e0c5ac88c6250e6332cbcb01f58e35639ae697b7c35f02fd54`  
		Last Modified: Mon, 28 Apr 2025 21:45:03 GMT  
		Size: 2.6 MB (2616138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16b11e87747e9af4e605b69f2e8b216d97192ebb98a146cf94c7e238e5d9e528`  
		Last Modified: Mon, 28 Apr 2025 21:45:02 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:78464a448a335f3cb82525499848a712f2453ae9cf8686f22da402706f29d72e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:8e9640f8fd8dcddf45b2b3f208e65efba5ad76f3b0516a83abe1812319b5bcca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105504221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a749249703327cbb17185e8cd68a4bbf0a55429bcdb75da7a6ee110641badf0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 25 Mar 2025 16:14:46 GMT
ENV EMQX_VERSION=5.8.6
# Tue, 25 Mar 2025 16:14:46 GMT
ENV AMD64_SHA256=430f69c24c0d659a9ce2e902d018c6dd20565519925e0cc893980d824b0a952e
# Tue, 25 Mar 2025 16:14:46 GMT
ENV ARM64_SHA256=dcabedb9d3888e0fb6e8138da6ae3d8ef1afce1f85e4580f26f19d65115ed5c3
# Tue, 25 Mar 2025 16:14:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 25 Mar 2025 16:14:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
WORKDIR /opt/emqx
# Tue, 25 Mar 2025 16:14:46 GMT
USER emqx
# Tue, 25 Mar 2025 16:14:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Mar 2025 16:14:46 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 25 Mar 2025 16:14:46 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 16:14:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07636c07c94e945b674445fd1c661d1107fc9dbf2bf0f8278215d255283e988`  
		Last Modified: Thu, 08 May 2025 17:24:28 GMT  
		Size: 77.3 MB (77275516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71f4f3a12090159d90e569c5161ed3c56c0458ec151718bfcf49bff73b930c2`  
		Last Modified: Thu, 08 May 2025 17:24:11 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:caff0cb09d946e6afab72667346f01a6fc2004b501d06c5fca9ae4b22a8f2b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ba7e3aa0d0f1ce3b7303677e2ead6d9618a402be77bf6549c6d4107217b158`

```dockerfile
```

-	Layers:
	-	`sha256:bfd76372ba86fbfd83f15b70c440f679d43e49b33e0eae9ea12b8f5a35e9513a`  
		Last Modified: Mon, 28 Apr 2025 21:42:18 GMT  
		Size: 2.6 MB (2615858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c1ebf69ed8a1872a88ed717829801ff4f307032890669ebe6f54c23e8e2295`  
		Last Modified: Mon, 28 Apr 2025 21:42:17 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:ff0e514dcb5d97d34836fb0f3557e43fc7187866798d41ffb9a74df562cc5630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102617680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764d92b8fe48d4d1237b48ef9b19282c9a28b682ed679aac129666529041b360`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 25 Mar 2025 16:14:46 GMT
ENV EMQX_VERSION=5.8.6
# Tue, 25 Mar 2025 16:14:46 GMT
ENV AMD64_SHA256=430f69c24c0d659a9ce2e902d018c6dd20565519925e0cc893980d824b0a952e
# Tue, 25 Mar 2025 16:14:46 GMT
ENV ARM64_SHA256=dcabedb9d3888e0fb6e8138da6ae3d8ef1afce1f85e4580f26f19d65115ed5c3
# Tue, 25 Mar 2025 16:14:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 25 Mar 2025 16:14:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
WORKDIR /opt/emqx
# Tue, 25 Mar 2025 16:14:46 GMT
USER emqx
# Tue, 25 Mar 2025 16:14:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Mar 2025 16:14:46 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 25 Mar 2025 16:14:46 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 16:14:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9407aa8b55deb4df74d0efe7e8b3f932d9b641efc8288fc8c66f2395d7efeb0b`  
		Last Modified: Thu, 08 May 2025 17:50:23 GMT  
		Size: 74.5 MB (74549996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f46b7da4817f32733b4919e3407cffec88d7835f7a9b46ccc58323abaf1163`  
		Last Modified: Thu, 08 May 2025 17:50:15 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:87b4132c9be52d9b48c8bdaf20edaca01c361d2987166cd80977e1f7cb86f3f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7858099c1efd8c3d562ecbe75873ad620019933de433168cdf92bb463d0f1ddc`

```dockerfile
```

-	Layers:
	-	`sha256:98e4fd22817af6e0c5ac88c6250e6332cbcb01f58e35639ae697b7c35f02fd54`  
		Last Modified: Mon, 28 Apr 2025 21:45:03 GMT  
		Size: 2.6 MB (2616138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16b11e87747e9af4e605b69f2e8b216d97192ebb98a146cf94c7e238e5d9e528`  
		Last Modified: Mon, 28 Apr 2025 21:45:02 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json
