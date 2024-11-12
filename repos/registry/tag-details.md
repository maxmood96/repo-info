<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.3`](#registry283)
-	[`registry:3.0.0-rc.1`](#registry300-rc1)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:8fbc5829dfb333ec2bc704681b6988ab4137dfa0976ee3395e8cf7c2ee150aaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:2` - linux; amd64

```console
$ docker pull registry@sha256:d252b0c9a9409bb1e10a98a6b79d8f2a082284a113bc33f49121bb2fb0797cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10114147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18a86d35e983225b84aae3bb15c84bd9e47506dd0102975c0ed97958703bb73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb0aa443e23aedd28f0818f7a18de9911383d0b9b621bc448070ded1d6c81c3`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 293.4 KB (293379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813676e291ef88d6de121b9a67d4b546585c87f2b89df39d4fd14ba984cd655f`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2fb7dcec6119c150b59df0550dc646f6a45351470a7b74f0a904df40418a12`  
		Last Modified: Tue, 12 Nov 2024 02:37:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916205650bfe545ec2ac378e84f53759e0c977a77e583f0525e05cf3c8923df5`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:ef807d6ab3ae145cb40e6bc86fbd8de0fb6f4c6726ac88e619634da80dd35994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 KB (193072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e7ad24d9321d0ba3df236bcc6d5bf0a26dc6b4069c58745f6d491db169526b`

```dockerfile
```

-	Layers:
	-	`sha256:547ee2ce16efcc56c2f70e31f7327b246f129ae9e0e0f5393b19da960f910466`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 179.0 KB (179007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e019b81fd4a44bcc35582450d9aeddbdb46be2e2b6e0e5bd6cbe0dcc431d8b`  
		Last Modified: Tue, 12 Nov 2024 02:37:05 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm variant v6

```console
$ docker pull registry@sha256:8351e958c42f9de2b77889506fae68712813fb6bc5f4e1579cf103bec35d41b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9477718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646ed268fea06904233caf5921a317743a80856db79e456db3956b70cc1a7b1b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-armhf.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:1ce61877166753d951080511a4649a7a9674d00fdd71569057a7f3099f39e6d8`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.2 MB (3158999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b739e776fe9e57644b5e4e99c00c4dbb4a039c894137288a095e5adcc3f78d8`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 294.0 KB (294026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5afee98ad80b18cdcc1e4f610c4b5f499b6c55c68ea75a4743e1e680fa910f4`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 6.0 MB (6024109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7f5e00a1807cf3e9f780608fcb4b45baf5e9735de16505b91749f287e31298`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adbb8c5936d65b71c7da2c2cabe8705bd496d982f440619bbe8c594d5c3f02d`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:2d1adb226ba38d47f5571423f8a72ab46d1e47a64a2274c699f648077cb956dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88f40fc59ce3d885eed54f4550aa108d5a9a860953d6fa19396d6bb55174da9`

```dockerfile
```

-	Layers:
	-	`sha256:5c26b5cde765c90b744538bf4a6ca95d05a2fb38fd9029fe5688ec806b0f1c18`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 13.9 KB (13939 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm variant v7

```console
$ docker pull registry@sha256:a35141fa557e56d01aaca3b4a6dd7bbd5a1514e1398d4df026803d536a8ff981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9222062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbfc84ca3886ce8e641b5fe1b3bb8f500bd61b6b0d74420780069e9d63af0b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:6a6f0b0819f0c6585d2f9ef4edf9dc22a3f7ee9cba3de0b83dffb8f2a14dc3f3 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:9747154b8e1c5a1d049032763040bd9a6319da995da6517c17ab2d18257f0aff`  
		Last Modified: Fri, 06 Sep 2024 22:08:45 GMT  
		Size: 2.9 MB (2911364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d12bbe20fd347eff00df815b9d08c22b4a53c1fdd063f10d2a9bed89d54341`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 292.9 KB (292902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b5204efc15665e2e28441b9823b61d33ef1311df237dc837a6fd2548824f6f`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 6.0 MB (6017211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f7526059fabbb222965febd50dfb4a96970304d28e8a790b2956d7c6a29b0`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbbb78297f7d059ce8a37e1aba0a85d9870d3ac98bf2f67147162160bf1b54a`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:9a63dc1083c69a80d388e3f972c8eb6654c773633d4cf28ec8f8f1421ba37f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 KB (192752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9a2ffdc404ccb2cca80e53fc36fcd9c3641583898ec0e09d72fef675ff2beb`

```dockerfile
```

-	Layers:
	-	`sha256:b6b056e660bb162a61a44677ef9c31e908db42c4b89113707ec5900b2aba98f7`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 178.8 KB (178831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76ef550ca1476a68f6d3d5e6987341665199a439793a97d323cba4fad15115f2`  
		Last Modified: Sat, 07 Sep 2024 12:43:50 GMT  
		Size: 13.9 KB (13921 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:1ef66c49c952ab0d20c905634d50d3a0da70133b0cdb52732a30a0fd89f01a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6adc34955df9f22da1fdc0474dcbab66dfce57ded89499201125f7dc1b9924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe29ef241d9fe87b99b77f4d96972773b3ae04f1a46c6fea0e0a60800f5f1e1`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 295.8 KB (295832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2787542bdb41f6b8315204be8ea01cb7ff82d9e6de97e9283e8af8dc6ce650e`  
		Last Modified: Tue, 12 Nov 2024 10:28:26 GMT  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b69fee0ac896543d4936d9c57aea16e665df781ec13ec5257f8bea258da7c79`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2de197705d02128cc248e6540d752209fe9ed73a32bfb6b19947205030524`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:bbf9ae6a42e4d8aef2759420301cfcc7ed642ba200ae3bf030fd5fdb9d0d2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8bd06db3380d6a4af9f2d942917235c0df5b1a02aec67120ee470ae2e11a94`

```dockerfile
```

-	Layers:
	-	`sha256:1b1f1a3aa2b9f06c429988bbdfa0c781210c0d81d6befa0769051742b9607830`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 179.1 KB (179063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a601ce5a2c5491c5fd401d93594ecbf76515407f52ce37185f82be3efee56e04`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; ppc64le

```console
$ docker pull registry@sha256:86cdf44fa43a89e6031fc50e516d886c0b257f9f8463548218f7aa0cddca35a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe03a1f8a043cc0d142b1dbfc0701eb12d5888e6714d95ef5de3ee3f66c3637`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-ppc64le.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bf19dcb5e2f7e7518032e1f3abc91f7a0f014fc0f3a03de278aca2c9a523ea4f`  
		Last Modified: Tue, 12 Nov 2024 00:56:06 GMT  
		Size: 3.4 MB (3358858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3792e3246e50751fd99db95bd81487f4ff267e527d2bdd744a8f15002029e84b`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 296.2 KB (296245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4725d46af85c7a6abba2419cef1cd0a36956cf13a020d059ba8751a3a0687006`  
		Last Modified: Tue, 12 Nov 2024 08:06:05 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6f196c518d25b0537d6b92276855a0f837b6f99bc09e9cd2854e83070c872`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6030f6d937516639db015c42c56128b1c45f80405aa31d885d4e91fc8cd0ea17`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:63ebe77f6c587302b3a687db1d46b6b9e8b5d89b573cfc083d1f9dad199991b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 KB (191198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e17de964dc185bfd1b49f65e7621e00c8c3a999513e31042bd22d6f293d26`

```dockerfile
```

-	Layers:
	-	`sha256:191655aad642e846fe9649b077d09cf1d11d1be5742cefe8be2036f8ceafe72f`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 177.1 KB (177087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47532ea0bac7cfc58e078cb792bdb9e1222186b96f8de6519bd95c04af4441b9`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; s390x

```console
$ docker pull registry@sha256:cad4fdf4a03376ba0904fafcb75e16e3468c10f61e3c64a4cfbb372470c8b891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7cccb184b781c20bdbb9ceff63cafb03db8074fdc32bac40da22617b729bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-s390x.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2cf6287c29b40fb867eb63db5d7189724563e69538ef303e15274f8139042129`  
		Last Modified: Tue, 12 Nov 2024 00:56:53 GMT  
		Size: 3.2 MB (3230439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149be30168d1b1aa8ec6b23c36dcdc39c2b2dcd978c5e0a2d8ca86109a0df7a`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 293.9 KB (293899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ded3165ca2acf8ea3ca820d45d88d54ade5de9f1264cc65acbe94b26d0b26`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878ae226c4b32247c8b552259cd2ff67e2c68b8c6dfe9af0b0785d28d04a9618`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277269a6b2649ecc19571438083237ee6b8b605bcb79eb5d2de467a0ab86a175`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:1c55fb5b8a1b682c0cb9ca173aa7fd36a7a8a0686c87592d298c085ba1bf31c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 KB (191118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8431cec168c6e8aeb1395b10dad52b6f9cdcadef36d4c1b5a36532ee574595ad`

```dockerfile
```

-	Layers:
	-	`sha256:7068d24c38f441b8c1a3dca81bc616b32e4c6eea0489aa2e68837a2b1d02973c`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 177.1 KB (177053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5953f2e3297796f4051786b247167696c4fdc409fca54425806f0ac4df56219`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8`

```console
$ docker pull registry@sha256:8fbc5829dfb333ec2bc704681b6988ab4137dfa0976ee3395e8cf7c2ee150aaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:2.8` - linux; amd64

```console
$ docker pull registry@sha256:d252b0c9a9409bb1e10a98a6b79d8f2a082284a113bc33f49121bb2fb0797cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10114147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18a86d35e983225b84aae3bb15c84bd9e47506dd0102975c0ed97958703bb73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb0aa443e23aedd28f0818f7a18de9911383d0b9b621bc448070ded1d6c81c3`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 293.4 KB (293379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813676e291ef88d6de121b9a67d4b546585c87f2b89df39d4fd14ba984cd655f`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2fb7dcec6119c150b59df0550dc646f6a45351470a7b74f0a904df40418a12`  
		Last Modified: Tue, 12 Nov 2024 02:37:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916205650bfe545ec2ac378e84f53759e0c977a77e583f0525e05cf3c8923df5`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:ef807d6ab3ae145cb40e6bc86fbd8de0fb6f4c6726ac88e619634da80dd35994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 KB (193072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e7ad24d9321d0ba3df236bcc6d5bf0a26dc6b4069c58745f6d491db169526b`

```dockerfile
```

-	Layers:
	-	`sha256:547ee2ce16efcc56c2f70e31f7327b246f129ae9e0e0f5393b19da960f910466`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 179.0 KB (179007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e019b81fd4a44bcc35582450d9aeddbdb46be2e2b6e0e5bd6cbe0dcc431d8b`  
		Last Modified: Tue, 12 Nov 2024 02:37:05 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm variant v6

```console
$ docker pull registry@sha256:8351e958c42f9de2b77889506fae68712813fb6bc5f4e1579cf103bec35d41b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9477718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646ed268fea06904233caf5921a317743a80856db79e456db3956b70cc1a7b1b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-armhf.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:1ce61877166753d951080511a4649a7a9674d00fdd71569057a7f3099f39e6d8`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.2 MB (3158999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b739e776fe9e57644b5e4e99c00c4dbb4a039c894137288a095e5adcc3f78d8`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 294.0 KB (294026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5afee98ad80b18cdcc1e4f610c4b5f499b6c55c68ea75a4743e1e680fa910f4`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 6.0 MB (6024109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7f5e00a1807cf3e9f780608fcb4b45baf5e9735de16505b91749f287e31298`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adbb8c5936d65b71c7da2c2cabe8705bd496d982f440619bbe8c594d5c3f02d`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:2d1adb226ba38d47f5571423f8a72ab46d1e47a64a2274c699f648077cb956dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88f40fc59ce3d885eed54f4550aa108d5a9a860953d6fa19396d6bb55174da9`

```dockerfile
```

-	Layers:
	-	`sha256:5c26b5cde765c90b744538bf4a6ca95d05a2fb38fd9029fe5688ec806b0f1c18`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 13.9 KB (13939 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm variant v7

```console
$ docker pull registry@sha256:a35141fa557e56d01aaca3b4a6dd7bbd5a1514e1398d4df026803d536a8ff981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9222062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbfc84ca3886ce8e641b5fe1b3bb8f500bd61b6b0d74420780069e9d63af0b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:6a6f0b0819f0c6585d2f9ef4edf9dc22a3f7ee9cba3de0b83dffb8f2a14dc3f3 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:9747154b8e1c5a1d049032763040bd9a6319da995da6517c17ab2d18257f0aff`  
		Last Modified: Fri, 06 Sep 2024 22:08:45 GMT  
		Size: 2.9 MB (2911364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d12bbe20fd347eff00df815b9d08c22b4a53c1fdd063f10d2a9bed89d54341`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 292.9 KB (292902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b5204efc15665e2e28441b9823b61d33ef1311df237dc837a6fd2548824f6f`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 6.0 MB (6017211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f7526059fabbb222965febd50dfb4a96970304d28e8a790b2956d7c6a29b0`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbbb78297f7d059ce8a37e1aba0a85d9870d3ac98bf2f67147162160bf1b54a`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:9a63dc1083c69a80d388e3f972c8eb6654c773633d4cf28ec8f8f1421ba37f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 KB (192752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9a2ffdc404ccb2cca80e53fc36fcd9c3641583898ec0e09d72fef675ff2beb`

```dockerfile
```

-	Layers:
	-	`sha256:b6b056e660bb162a61a44677ef9c31e908db42c4b89113707ec5900b2aba98f7`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 178.8 KB (178831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76ef550ca1476a68f6d3d5e6987341665199a439793a97d323cba4fad15115f2`  
		Last Modified: Sat, 07 Sep 2024 12:43:50 GMT  
		Size: 13.9 KB (13921 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:1ef66c49c952ab0d20c905634d50d3a0da70133b0cdb52732a30a0fd89f01a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6adc34955df9f22da1fdc0474dcbab66dfce57ded89499201125f7dc1b9924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe29ef241d9fe87b99b77f4d96972773b3ae04f1a46c6fea0e0a60800f5f1e1`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 295.8 KB (295832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2787542bdb41f6b8315204be8ea01cb7ff82d9e6de97e9283e8af8dc6ce650e`  
		Last Modified: Tue, 12 Nov 2024 10:28:26 GMT  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b69fee0ac896543d4936d9c57aea16e665df781ec13ec5257f8bea258da7c79`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2de197705d02128cc248e6540d752209fe9ed73a32bfb6b19947205030524`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:bbf9ae6a42e4d8aef2759420301cfcc7ed642ba200ae3bf030fd5fdb9d0d2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8bd06db3380d6a4af9f2d942917235c0df5b1a02aec67120ee470ae2e11a94`

```dockerfile
```

-	Layers:
	-	`sha256:1b1f1a3aa2b9f06c429988bbdfa0c781210c0d81d6befa0769051742b9607830`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 179.1 KB (179063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a601ce5a2c5491c5fd401d93594ecbf76515407f52ce37185f82be3efee56e04`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; ppc64le

```console
$ docker pull registry@sha256:86cdf44fa43a89e6031fc50e516d886c0b257f9f8463548218f7aa0cddca35a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe03a1f8a043cc0d142b1dbfc0701eb12d5888e6714d95ef5de3ee3f66c3637`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-ppc64le.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bf19dcb5e2f7e7518032e1f3abc91f7a0f014fc0f3a03de278aca2c9a523ea4f`  
		Last Modified: Tue, 12 Nov 2024 00:56:06 GMT  
		Size: 3.4 MB (3358858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3792e3246e50751fd99db95bd81487f4ff267e527d2bdd744a8f15002029e84b`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 296.2 KB (296245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4725d46af85c7a6abba2419cef1cd0a36956cf13a020d059ba8751a3a0687006`  
		Last Modified: Tue, 12 Nov 2024 08:06:05 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6f196c518d25b0537d6b92276855a0f837b6f99bc09e9cd2854e83070c872`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6030f6d937516639db015c42c56128b1c45f80405aa31d885d4e91fc8cd0ea17`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:63ebe77f6c587302b3a687db1d46b6b9e8b5d89b573cfc083d1f9dad199991b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 KB (191198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e17de964dc185bfd1b49f65e7621e00c8c3a999513e31042bd22d6f293d26`

```dockerfile
```

-	Layers:
	-	`sha256:191655aad642e846fe9649b077d09cf1d11d1be5742cefe8be2036f8ceafe72f`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 177.1 KB (177087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47532ea0bac7cfc58e078cb792bdb9e1222186b96f8de6519bd95c04af4441b9`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; s390x

```console
$ docker pull registry@sha256:cad4fdf4a03376ba0904fafcb75e16e3468c10f61e3c64a4cfbb372470c8b891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7cccb184b781c20bdbb9ceff63cafb03db8074fdc32bac40da22617b729bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-s390x.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2cf6287c29b40fb867eb63db5d7189724563e69538ef303e15274f8139042129`  
		Last Modified: Tue, 12 Nov 2024 00:56:53 GMT  
		Size: 3.2 MB (3230439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149be30168d1b1aa8ec6b23c36dcdc39c2b2dcd978c5e0a2d8ca86109a0df7a`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 293.9 KB (293899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ded3165ca2acf8ea3ca820d45d88d54ade5de9f1264cc65acbe94b26d0b26`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878ae226c4b32247c8b552259cd2ff67e2c68b8c6dfe9af0b0785d28d04a9618`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277269a6b2649ecc19571438083237ee6b8b605bcb79eb5d2de467a0ab86a175`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:1c55fb5b8a1b682c0cb9ca173aa7fd36a7a8a0686c87592d298c085ba1bf31c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 KB (191118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8431cec168c6e8aeb1395b10dad52b6f9cdcadef36d4c1b5a36532ee574595ad`

```dockerfile
```

-	Layers:
	-	`sha256:7068d24c38f441b8c1a3dca81bc616b32e4c6eea0489aa2e68837a2b1d02973c`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 177.1 KB (177053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5953f2e3297796f4051786b247167696c4fdc409fca54425806f0ac4df56219`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8.3`

```console
$ docker pull registry@sha256:8fbc5829dfb333ec2bc704681b6988ab4137dfa0976ee3395e8cf7c2ee150aaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:2.8.3` - linux; amd64

```console
$ docker pull registry@sha256:d252b0c9a9409bb1e10a98a6b79d8f2a082284a113bc33f49121bb2fb0797cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10114147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18a86d35e983225b84aae3bb15c84bd9e47506dd0102975c0ed97958703bb73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb0aa443e23aedd28f0818f7a18de9911383d0b9b621bc448070ded1d6c81c3`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 293.4 KB (293379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813676e291ef88d6de121b9a67d4b546585c87f2b89df39d4fd14ba984cd655f`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2fb7dcec6119c150b59df0550dc646f6a45351470a7b74f0a904df40418a12`  
		Last Modified: Tue, 12 Nov 2024 02:37:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916205650bfe545ec2ac378e84f53759e0c977a77e583f0525e05cf3c8923df5`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:ef807d6ab3ae145cb40e6bc86fbd8de0fb6f4c6726ac88e619634da80dd35994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 KB (193072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e7ad24d9321d0ba3df236bcc6d5bf0a26dc6b4069c58745f6d491db169526b`

```dockerfile
```

-	Layers:
	-	`sha256:547ee2ce16efcc56c2f70e31f7327b246f129ae9e0e0f5393b19da960f910466`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 179.0 KB (179007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e019b81fd4a44bcc35582450d9aeddbdb46be2e2b6e0e5bd6cbe0dcc431d8b`  
		Last Modified: Tue, 12 Nov 2024 02:37:05 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm variant v6

```console
$ docker pull registry@sha256:8351e958c42f9de2b77889506fae68712813fb6bc5f4e1579cf103bec35d41b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9477718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646ed268fea06904233caf5921a317743a80856db79e456db3956b70cc1a7b1b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-armhf.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:1ce61877166753d951080511a4649a7a9674d00fdd71569057a7f3099f39e6d8`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.2 MB (3158999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b739e776fe9e57644b5e4e99c00c4dbb4a039c894137288a095e5adcc3f78d8`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 294.0 KB (294026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5afee98ad80b18cdcc1e4f610c4b5f499b6c55c68ea75a4743e1e680fa910f4`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 6.0 MB (6024109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7f5e00a1807cf3e9f780608fcb4b45baf5e9735de16505b91749f287e31298`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adbb8c5936d65b71c7da2c2cabe8705bd496d982f440619bbe8c594d5c3f02d`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:2d1adb226ba38d47f5571423f8a72ab46d1e47a64a2274c699f648077cb956dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88f40fc59ce3d885eed54f4550aa108d5a9a860953d6fa19396d6bb55174da9`

```dockerfile
```

-	Layers:
	-	`sha256:5c26b5cde765c90b744538bf4a6ca95d05a2fb38fd9029fe5688ec806b0f1c18`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 13.9 KB (13939 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm variant v7

```console
$ docker pull registry@sha256:a35141fa557e56d01aaca3b4a6dd7bbd5a1514e1398d4df026803d536a8ff981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9222062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbfc84ca3886ce8e641b5fe1b3bb8f500bd61b6b0d74420780069e9d63af0b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:6a6f0b0819f0c6585d2f9ef4edf9dc22a3f7ee9cba3de0b83dffb8f2a14dc3f3 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:9747154b8e1c5a1d049032763040bd9a6319da995da6517c17ab2d18257f0aff`  
		Last Modified: Fri, 06 Sep 2024 22:08:45 GMT  
		Size: 2.9 MB (2911364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d12bbe20fd347eff00df815b9d08c22b4a53c1fdd063f10d2a9bed89d54341`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 292.9 KB (292902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b5204efc15665e2e28441b9823b61d33ef1311df237dc837a6fd2548824f6f`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 6.0 MB (6017211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f7526059fabbb222965febd50dfb4a96970304d28e8a790b2956d7c6a29b0`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbbb78297f7d059ce8a37e1aba0a85d9870d3ac98bf2f67147162160bf1b54a`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:9a63dc1083c69a80d388e3f972c8eb6654c773633d4cf28ec8f8f1421ba37f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 KB (192752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9a2ffdc404ccb2cca80e53fc36fcd9c3641583898ec0e09d72fef675ff2beb`

```dockerfile
```

-	Layers:
	-	`sha256:b6b056e660bb162a61a44677ef9c31e908db42c4b89113707ec5900b2aba98f7`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 178.8 KB (178831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76ef550ca1476a68f6d3d5e6987341665199a439793a97d323cba4fad15115f2`  
		Last Modified: Sat, 07 Sep 2024 12:43:50 GMT  
		Size: 13.9 KB (13921 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:1ef66c49c952ab0d20c905634d50d3a0da70133b0cdb52732a30a0fd89f01a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6adc34955df9f22da1fdc0474dcbab66dfce57ded89499201125f7dc1b9924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe29ef241d9fe87b99b77f4d96972773b3ae04f1a46c6fea0e0a60800f5f1e1`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 295.8 KB (295832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2787542bdb41f6b8315204be8ea01cb7ff82d9e6de97e9283e8af8dc6ce650e`  
		Last Modified: Tue, 12 Nov 2024 10:28:26 GMT  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b69fee0ac896543d4936d9c57aea16e665df781ec13ec5257f8bea258da7c79`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2de197705d02128cc248e6540d752209fe9ed73a32bfb6b19947205030524`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:bbf9ae6a42e4d8aef2759420301cfcc7ed642ba200ae3bf030fd5fdb9d0d2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8bd06db3380d6a4af9f2d942917235c0df5b1a02aec67120ee470ae2e11a94`

```dockerfile
```

-	Layers:
	-	`sha256:1b1f1a3aa2b9f06c429988bbdfa0c781210c0d81d6befa0769051742b9607830`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 179.1 KB (179063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a601ce5a2c5491c5fd401d93594ecbf76515407f52ce37185f82be3efee56e04`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; ppc64le

```console
$ docker pull registry@sha256:86cdf44fa43a89e6031fc50e516d886c0b257f9f8463548218f7aa0cddca35a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe03a1f8a043cc0d142b1dbfc0701eb12d5888e6714d95ef5de3ee3f66c3637`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-ppc64le.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bf19dcb5e2f7e7518032e1f3abc91f7a0f014fc0f3a03de278aca2c9a523ea4f`  
		Last Modified: Tue, 12 Nov 2024 00:56:06 GMT  
		Size: 3.4 MB (3358858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3792e3246e50751fd99db95bd81487f4ff267e527d2bdd744a8f15002029e84b`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 296.2 KB (296245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4725d46af85c7a6abba2419cef1cd0a36956cf13a020d059ba8751a3a0687006`  
		Last Modified: Tue, 12 Nov 2024 08:06:05 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6f196c518d25b0537d6b92276855a0f837b6f99bc09e9cd2854e83070c872`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6030f6d937516639db015c42c56128b1c45f80405aa31d885d4e91fc8cd0ea17`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:63ebe77f6c587302b3a687db1d46b6b9e8b5d89b573cfc083d1f9dad199991b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 KB (191198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e17de964dc185bfd1b49f65e7621e00c8c3a999513e31042bd22d6f293d26`

```dockerfile
```

-	Layers:
	-	`sha256:191655aad642e846fe9649b077d09cf1d11d1be5742cefe8be2036f8ceafe72f`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 177.1 KB (177087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47532ea0bac7cfc58e078cb792bdb9e1222186b96f8de6519bd95c04af4441b9`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; s390x

```console
$ docker pull registry@sha256:cad4fdf4a03376ba0904fafcb75e16e3468c10f61e3c64a4cfbb372470c8b891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7cccb184b781c20bdbb9ceff63cafb03db8074fdc32bac40da22617b729bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-s390x.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2cf6287c29b40fb867eb63db5d7189724563e69538ef303e15274f8139042129`  
		Last Modified: Tue, 12 Nov 2024 00:56:53 GMT  
		Size: 3.2 MB (3230439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149be30168d1b1aa8ec6b23c36dcdc39c2b2dcd978c5e0a2d8ca86109a0df7a`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 293.9 KB (293899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ded3165ca2acf8ea3ca820d45d88d54ade5de9f1264cc65acbe94b26d0b26`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878ae226c4b32247c8b552259cd2ff67e2c68b8c6dfe9af0b0785d28d04a9618`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277269a6b2649ecc19571438083237ee6b8b605bcb79eb5d2de467a0ab86a175`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:1c55fb5b8a1b682c0cb9ca173aa7fd36a7a8a0686c87592d298c085ba1bf31c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 KB (191118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8431cec168c6e8aeb1395b10dad52b6f9cdcadef36d4c1b5a36532ee574595ad`

```dockerfile
```

-	Layers:
	-	`sha256:7068d24c38f441b8c1a3dca81bc616b32e4c6eea0489aa2e68837a2b1d02973c`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 177.1 KB (177053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5953f2e3297796f4051786b247167696c4fdc409fca54425806f0ac4df56219`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:3.0.0-rc.1`

```console
$ docker pull registry@sha256:61dc60e137e379f89194bbabcfdc184eaa4a531edbdc300ccb904e2a3b547159
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:3.0.0-rc.1` - linux; amd64

```console
$ docker pull registry@sha256:34ac8664568f4d687dc50aaff95db4e77e43f031d2084fbd76fcb6049346b58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18233263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9da24547faae15ec446b120f2582fd751d2b1036a6a09b34d49f9affd6842d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 08 Nov 2024 07:29:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
RUN set -eux; 	version='3.0.0-rc.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='ca7a81752601dcfbc6e6c00fb5b87fd117ac35553e3025b40033e03945077bb0' ;; 		aarch64) arch='arm64';   sha256='47b45df09919e89091c7e9225b92b75b41fe6bdf5767793a26de011c046f88e3' ;; 		armhf)   arch='armv6';   sha256='6cbf67de5f0e2927f0a4e0863bbc88f8831aaf94348c2f930a411aebcb6ca694' ;; 		armv7)   arch='armv7';   sha256='4819de376733af19427ce4f5b0944db195f0e5f8bfd93e46e6c5784ad50d53b6' ;; 		ppc64le) arch='ppc64le'; sha256='3289e9012133947f28a85c29f667755f6ad63856dd3b8891aa5a46443813a3f7' ;; 		s390x)   arch='s390x';   sha256='2d0026e09fec4b0bd4dafddf6ab1b22c6ea19ab49c866ec0ec8dd8fe12f6ef21' ;;                 riscv64) arch='riscv64'; sha256='32ae070e57596dab3b23dd48877069792a70fe13e9b429c498cfee6b56be860a' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
VOLUME [/var/lib/registry]
# Fri, 08 Nov 2024 07:29:49 GMT
EXPOSE map[5000/tcp:{}]
# Fri, 08 Nov 2024 07:29:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Nov 2024 07:29:49 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22c0d7190e75757280eb9566c44c267f36c21e5614ddf78e9bd21ac2d4e61bd`  
		Last Modified: Tue, 12 Nov 2024 02:37:07 GMT  
		Size: 290.9 KB (290889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14c66978d04c3d95030ebbefc93c2f0bca23bf4d12664d556c484d2eb7eabf1`  
		Last Modified: Tue, 12 Nov 2024 02:37:08 GMT  
		Size: 14.3 MB (14317861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be567d4e80794da3bba7569539928990902d6b32042bebb8006f91c9ab9db25f`  
		Last Modified: Tue, 12 Nov 2024 02:37:07 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916205650bfe545ec2ac378e84f53759e0c977a77e583f0525e05cf3c8923df5`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.1` - unknown; unknown

```console
$ docker pull registry@sha256:56e9f7a2a4cc7ae1bf0d2d8fe3fa03478f07350768d745afff701ca0d705ccce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 KB (271880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c62f2354cc268502fc411fe2c03a2f08f51fefdd75b29cd24f1bf0397fffd3b`

```dockerfile
```

-	Layers:
	-	`sha256:794accd823fbb4ef921aabba8a4330b174670aea6f533fb92ef147bc660e3de4`  
		Last Modified: Tue, 12 Nov 2024 02:37:07 GMT  
		Size: 258.4 KB (258391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c72075b916538f5be261f18bb2fb739a15efa0f92139d2fec9473b43d5e66b81`  
		Last Modified: Tue, 12 Nov 2024 02:37:07 GMT  
		Size: 13.5 KB (13489 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.1` - linux; arm variant v6

```console
$ docker pull registry@sha256:bd05857c7c37ff2c7bd748e3b46a13baffa4aba9baa87b881cf6bfad8145fbaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17115176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcb754f54415f2d295b50119482ba78bd4c213374bf180ee553d8bf0f6b495b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 08 Nov 2024 07:29:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
RUN set -eux; 	version='3.0.0-rc.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='ca7a81752601dcfbc6e6c00fb5b87fd117ac35553e3025b40033e03945077bb0' ;; 		aarch64) arch='arm64';   sha256='47b45df09919e89091c7e9225b92b75b41fe6bdf5767793a26de011c046f88e3' ;; 		armhf)   arch='armv6';   sha256='6cbf67de5f0e2927f0a4e0863bbc88f8831aaf94348c2f930a411aebcb6ca694' ;; 		armv7)   arch='armv7';   sha256='4819de376733af19427ce4f5b0944db195f0e5f8bfd93e46e6c5784ad50d53b6' ;; 		ppc64le) arch='ppc64le'; sha256='3289e9012133947f28a85c29f667755f6ad63856dd3b8891aa5a46443813a3f7' ;; 		s390x)   arch='s390x';   sha256='2d0026e09fec4b0bd4dafddf6ab1b22c6ea19ab49c866ec0ec8dd8fe12f6ef21' ;;                 riscv64) arch='riscv64'; sha256='32ae070e57596dab3b23dd48877069792a70fe13e9b429c498cfee6b56be860a' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
VOLUME [/var/lib/registry]
# Fri, 08 Nov 2024 07:29:49 GMT
EXPOSE map[5000/tcp:{}]
# Fri, 08 Nov 2024 07:29:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Nov 2024 07:29:49 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09660efa60074dd6fc7ed0eaa983537498c86f66f4ce6ec6fd9caf5018feac3`  
		Last Modified: Tue, 12 Nov 2024 06:28:18 GMT  
		Size: 291.8 KB (291778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2551c96ec982be698248dff14584d5133e087a20b477eecdb7533ef852c751f`  
		Last Modified: Tue, 12 Nov 2024 06:28:19 GMT  
		Size: 13.5 MB (13456188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2122b290fb029c93fa03d0ad52bbc17797ddeae75b69614983d55b76c3c0407`  
		Last Modified: Tue, 12 Nov 2024 06:28:18 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee4c77c5e993746f64eccbcd6b11ec93c15a6fd5b46c0065d3c5674835baa32`  
		Last Modified: Fri, 08 Nov 2024 21:58:33 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.1` - unknown; unknown

```console
$ docker pull registry@sha256:252978ab3369e6afaa553f7885d25757738e526639f57efb9e945da97669da85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13955e016c2e70b22f1821d581673b6d0bf818f0c0bc8f40bdefba5c6def8633`

```dockerfile
```

-	Layers:
	-	`sha256:f41811f6016a3b157c00aba82ea9d6c52a651fcc08b27ed6f154af137f6f09c0`  
		Last Modified: Tue, 12 Nov 2024 06:28:18 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.1` - linux; arm variant v7

```console
$ docker pull registry@sha256:0e5d59d29eb079950815fd85f1a4f2d5c4863b86d03565707a9bbc613fa89172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16837623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc9829e833fe58a0e3ace7eacfd3c9ea18f7418ca119d9930c43ce706d2d352`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 08 Nov 2024 07:29:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
RUN set -eux; 	version='3.0.0-rc.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='ca7a81752601dcfbc6e6c00fb5b87fd117ac35553e3025b40033e03945077bb0' ;; 		aarch64) arch='arm64';   sha256='47b45df09919e89091c7e9225b92b75b41fe6bdf5767793a26de011c046f88e3' ;; 		armhf)   arch='armv6';   sha256='6cbf67de5f0e2927f0a4e0863bbc88f8831aaf94348c2f930a411aebcb6ca694' ;; 		armv7)   arch='armv7';   sha256='4819de376733af19427ce4f5b0944db195f0e5f8bfd93e46e6c5784ad50d53b6' ;; 		ppc64le) arch='ppc64le'; sha256='3289e9012133947f28a85c29f667755f6ad63856dd3b8891aa5a46443813a3f7' ;; 		s390x)   arch='s390x';   sha256='2d0026e09fec4b0bd4dafddf6ab1b22c6ea19ab49c866ec0ec8dd8fe12f6ef21' ;;                 riscv64) arch='riscv64'; sha256='32ae070e57596dab3b23dd48877069792a70fe13e9b429c498cfee6b56be860a' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
VOLUME [/var/lib/registry]
# Fri, 08 Nov 2024 07:29:49 GMT
EXPOSE map[5000/tcp:{}]
# Fri, 08 Nov 2024 07:29:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Nov 2024 07:29:49 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692a5c99cf15c99e5e68f32ee94771988d92aa96b54f7c87c6ca7ecd4a4c3ef9`  
		Last Modified: Thu, 07 Nov 2024 03:01:47 GMT  
		Size: 291.0 KB (290959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915285cc28818eca5f39d9d5ce7a6e51e4b6c9fe64ae1654b57c7033483745fa`  
		Last Modified: Fri, 08 Nov 2024 21:58:38 GMT  
		Size: 13.5 MB (13450551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc4b3e14d12e63692801bccf92e6a6c00f7eb8fe214f70e01331c9eae853952`  
		Last Modified: Fri, 08 Nov 2024 21:58:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114df6f65c80c565b6d30a03082b3d6d011b459d166c0ccbccfe5790b31ef551`  
		Last Modified: Fri, 08 Nov 2024 21:58:37 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.1` - unknown; unknown

```console
$ docker pull registry@sha256:a278407f52f8a61ef0f04b694bd9b5cdb857ac8d2eed4d5ba91ab4f31fae4016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 KB (271758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634ab2cffd723e2144ae5589c1129b4dab53bf618ff3a7716dd0630736cebcdd`

```dockerfile
```

-	Layers:
	-	`sha256:9c90d360fa0f0b1cc76245c301e7dfc00b0757e00464bf4c8e4d6a20f4593ab4`  
		Last Modified: Fri, 08 Nov 2024 21:58:38 GMT  
		Size: 258.4 KB (258403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4108fe8fa4be2b2622e1531f8fbe54aef6ce1963328bc6100fe4ce09253aff3`  
		Last Modified: Fri, 08 Nov 2024 21:58:37 GMT  
		Size: 13.4 KB (13355 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.1` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:b3cb0d0e52438c43b8ba48477d0a31cc578a0beb0e052d324a4b5370db35d288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17603437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23bb83dbd2403599c60c7f6c502bfd0ce7bc98f2deb9570b10b50c495205d9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 08 Nov 2024 07:29:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
RUN set -eux; 	version='3.0.0-rc.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='ca7a81752601dcfbc6e6c00fb5b87fd117ac35553e3025b40033e03945077bb0' ;; 		aarch64) arch='arm64';   sha256='47b45df09919e89091c7e9225b92b75b41fe6bdf5767793a26de011c046f88e3' ;; 		armhf)   arch='armv6';   sha256='6cbf67de5f0e2927f0a4e0863bbc88f8831aaf94348c2f930a411aebcb6ca694' ;; 		armv7)   arch='armv7';   sha256='4819de376733af19427ce4f5b0944db195f0e5f8bfd93e46e6c5784ad50d53b6' ;; 		ppc64le) arch='ppc64le'; sha256='3289e9012133947f28a85c29f667755f6ad63856dd3b8891aa5a46443813a3f7' ;; 		s390x)   arch='s390x';   sha256='2d0026e09fec4b0bd4dafddf6ab1b22c6ea19ab49c866ec0ec8dd8fe12f6ef21' ;;                 riscv64) arch='riscv64'; sha256='32ae070e57596dab3b23dd48877069792a70fe13e9b429c498cfee6b56be860a' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
VOLUME [/var/lib/registry]
# Fri, 08 Nov 2024 07:29:49 GMT
EXPOSE map[5000/tcp:{}]
# Fri, 08 Nov 2024 07:29:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Nov 2024 07:29:49 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d571ba9261b2ec97b6a5261bc2b5f8dd6b1cad7aa5ab454e38fdd9ab1cf45335`  
		Last Modified: Tue, 12 Nov 2024 10:27:52 GMT  
		Size: 293.5 KB (293522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90435b08ed86201d6bfb51a21d7c14079f2f9c91cd8c8414ea453944025eebf`  
		Last Modified: Tue, 12 Nov 2024 10:27:53 GMT  
		Size: 13.2 MB (13221578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f49fb0c620bd82f416639bc80de115db8a25cd768301bbaa9643b23b834f11`  
		Last Modified: Tue, 12 Nov 2024 10:27:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7028b3f3c03d1fdeb7b585142f78032e680225ca7e5e27472e6dca08e7205d7`  
		Last Modified: Tue, 12 Nov 2024 10:27:52 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.1` - unknown; unknown

```console
$ docker pull registry@sha256:0bb3772201768eb7919c5b05342bf0192299516a811080e3acc302689c320c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 KB (271983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3518bdf8cc7fd8fbca9001318bfc1bbf46d1dba3bb73938b4481c26166dd17f5`

```dockerfile
```

-	Layers:
	-	`sha256:05a96d32c4fe94939063b95adaa959e3ac238c82049448bbf381a60691103177`  
		Last Modified: Tue, 12 Nov 2024 10:27:52 GMT  
		Size: 258.4 KB (258411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868b68a3cb7d45e79fcce3390d2722e1605af0384b012fdfedb03b5842f0d764`  
		Last Modified: Tue, 12 Nov 2024 10:27:52 GMT  
		Size: 13.6 KB (13572 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.1` - linux; ppc64le

```console
$ docker pull registry@sha256:db7556bf3bc12bdcda451ed6d1269ab674a4a3543cb27c77df53a0c5e323d315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16766698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1821e53703802b50fbbebd443c5935929d7348b4b96459b2f3e4f56b1471a3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 08 Nov 2024 07:29:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
RUN set -eux; 	version='3.0.0-rc.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='ca7a81752601dcfbc6e6c00fb5b87fd117ac35553e3025b40033e03945077bb0' ;; 		aarch64) arch='arm64';   sha256='47b45df09919e89091c7e9225b92b75b41fe6bdf5767793a26de011c046f88e3' ;; 		armhf)   arch='armv6';   sha256='6cbf67de5f0e2927f0a4e0863bbc88f8831aaf94348c2f930a411aebcb6ca694' ;; 		armv7)   arch='armv7';   sha256='4819de376733af19427ce4f5b0944db195f0e5f8bfd93e46e6c5784ad50d53b6' ;; 		ppc64le) arch='ppc64le'; sha256='3289e9012133947f28a85c29f667755f6ad63856dd3b8891aa5a46443813a3f7' ;; 		s390x)   arch='s390x';   sha256='2d0026e09fec4b0bd4dafddf6ab1b22c6ea19ab49c866ec0ec8dd8fe12f6ef21' ;;                 riscv64) arch='riscv64'; sha256='32ae070e57596dab3b23dd48877069792a70fe13e9b429c498cfee6b56be860a' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
VOLUME [/var/lib/registry]
# Fri, 08 Nov 2024 07:29:49 GMT
EXPOSE map[5000/tcp:{}]
# Fri, 08 Nov 2024 07:29:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Nov 2024 07:29:49 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3873bb4db6d014ff18a3c4d7f5d4ef80493c562c62c0640979ceafbca23930d`  
		Last Modified: Tue, 12 Nov 2024 08:05:08 GMT  
		Size: 294.0 KB (294032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f507abc8a6cbc28a7fa53975bf809a74a07cfe92d603aff227ab0e13c03c6790`  
		Last Modified: Tue, 12 Nov 2024 08:05:09 GMT  
		Size: 12.9 MB (12899598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3986f696008ae5376875969f9d2d26a79698533a76f05d804335f4227a0e6e07`  
		Last Modified: Tue, 12 Nov 2024 08:05:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211ed88e3eb155a901357bfdee3d4cdabe0f6c28405fbd594f52f546855d2c12`  
		Last Modified: Tue, 12 Nov 2024 08:05:08 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.1` - unknown; unknown

```console
$ docker pull registry@sha256:82bf2da07925a48a2b4b7ea677d39a5e3acb86cb6041187a90ab652a70f8271e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 KB (269970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca569ad43f933ff7dbec7324c102b98381c9c80350b72be738faa56dfee742a7`

```dockerfile
```

-	Layers:
	-	`sha256:2b66f117ab07e0d25777aadd3d3a74f77b9b4d0f44cf03e6ab78fa5cdd37275a`  
		Last Modified: Tue, 12 Nov 2024 08:05:09 GMT  
		Size: 256.5 KB (256453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2335863368b1cf75bcc32926a54dd698c6442b3b281ad951630120e53618e5b`  
		Last Modified: Tue, 12 Nov 2024 08:05:08 GMT  
		Size: 13.5 KB (13517 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.1` - linux; riscv64

```console
$ docker pull registry@sha256:58ddd494eddd406766bbabe98ce03fa824880075add79d742a9ab918dafc9502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17278196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dd9e8817233b5c5dca40ebf11b949d7023f104a3ceba295962bc7a676b38b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Fri, 08 Nov 2024 07:29:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
RUN set -eux; 	version='3.0.0-rc.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='ca7a81752601dcfbc6e6c00fb5b87fd117ac35553e3025b40033e03945077bb0' ;; 		aarch64) arch='arm64';   sha256='47b45df09919e89091c7e9225b92b75b41fe6bdf5767793a26de011c046f88e3' ;; 		armhf)   arch='armv6';   sha256='6cbf67de5f0e2927f0a4e0863bbc88f8831aaf94348c2f930a411aebcb6ca694' ;; 		armv7)   arch='armv7';   sha256='4819de376733af19427ce4f5b0944db195f0e5f8bfd93e46e6c5784ad50d53b6' ;; 		ppc64le) arch='ppc64le'; sha256='3289e9012133947f28a85c29f667755f6ad63856dd3b8891aa5a46443813a3f7' ;; 		s390x)   arch='s390x';   sha256='2d0026e09fec4b0bd4dafddf6ab1b22c6ea19ab49c866ec0ec8dd8fe12f6ef21' ;;                 riscv64) arch='riscv64'; sha256='32ae070e57596dab3b23dd48877069792a70fe13e9b429c498cfee6b56be860a' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
VOLUME [/var/lib/registry]
# Fri, 08 Nov 2024 07:29:49 GMT
EXPOSE map[5000/tcp:{}]
# Fri, 08 Nov 2024 07:29:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Nov 2024 07:29:49 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d1647e2ae8eb941891fcb716820e5bec12b348afc0d29dbe6ad642a22cf24a`  
		Last Modified: Sat, 07 Sep 2024 18:50:29 GMT  
		Size: 291.7 KB (291675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9faf1bf017abfdb1b8f72b8f472268f3d4c173d993f408dff4459284b684095`  
		Last Modified: Fri, 08 Nov 2024 22:00:41 GMT  
		Size: 13.6 MB (13614459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692cf651780de4847086e596def75409ca23a446032dd618a85e46dbd3c6d7ad`  
		Last Modified: Fri, 08 Nov 2024 22:00:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21ef716356ca9548a8ac7b7fd250edc7f1e78179554c547234ab0717b9b70fb`  
		Last Modified: Fri, 08 Nov 2024 22:00:39 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.1` - unknown; unknown

```console
$ docker pull registry@sha256:be4fd594b95abe3fe9941a1133c19e5ff54453c8eed17c2d9d3a3607d66e7fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 KB (269767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4644b54864bb09657b4987e791c0cfe48df1cc8e00a7fa103c1e824453b406aa`

```dockerfile
```

-	Layers:
	-	`sha256:26c377cfc7f6eb283345c110f7aada98bf1f96ba02c4b36e7cd76ba355b4407b`  
		Last Modified: Fri, 08 Nov 2024 22:00:39 GMT  
		Size: 256.4 KB (256449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1019e701adea3c807b83619f92315de5ccf2fe995288425b076e588219adf0b`  
		Last Modified: Fri, 08 Nov 2024 22:00:39 GMT  
		Size: 13.3 KB (13318 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.1` - linux; s390x

```console
$ docker pull registry@sha256:9cd4f54cd4a6b3884a38dce6ffab272d06522f86b6d8582d2052fefe226d9192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17544070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ef11119f92cd8f04f78d9747a7e167568b20085f8114cabc09d14371977aa7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 08 Nov 2024 07:29:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
RUN set -eux; 	version='3.0.0-rc.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='ca7a81752601dcfbc6e6c00fb5b87fd117ac35553e3025b40033e03945077bb0' ;; 		aarch64) arch='arm64';   sha256='47b45df09919e89091c7e9225b92b75b41fe6bdf5767793a26de011c046f88e3' ;; 		armhf)   arch='armv6';   sha256='6cbf67de5f0e2927f0a4e0863bbc88f8831aaf94348c2f930a411aebcb6ca694' ;; 		armv7)   arch='armv7';   sha256='4819de376733af19427ce4f5b0944db195f0e5f8bfd93e46e6c5784ad50d53b6' ;; 		ppc64le) arch='ppc64le'; sha256='3289e9012133947f28a85c29f667755f6ad63856dd3b8891aa5a46443813a3f7' ;; 		s390x)   arch='s390x';   sha256='2d0026e09fec4b0bd4dafddf6ab1b22c6ea19ab49c866ec0ec8dd8fe12f6ef21' ;;                 riscv64) arch='riscv64'; sha256='32ae070e57596dab3b23dd48877069792a70fe13e9b429c498cfee6b56be860a' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
VOLUME [/var/lib/registry]
# Fri, 08 Nov 2024 07:29:49 GMT
EXPOSE map[5000/tcp:{}]
# Fri, 08 Nov 2024 07:29:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 Nov 2024 07:29:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Nov 2024 07:29:49 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140cf6f32a5dac327c76fa8577bc2bd58aa8dbef28f69659ae30a5ae04e176c2`  
		Last Modified: Tue, 12 Nov 2024 08:40:30 GMT  
		Size: 291.9 KB (291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ddab78443389eecec4538073b84ae57288f6b0e71a14bb0888f92950dc9135`  
		Last Modified: Tue, 12 Nov 2024 08:40:30 GMT  
		Size: 13.8 MB (13789953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b80a902b67248cb4d7518c44779d92943f9bf43e5ba9d276dc1da960e1dc93`  
		Last Modified: Tue, 12 Nov 2024 08:40:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc775001589b31e7cf957e56319302eb143180f0076bf8fa515e27e53910bfcf`  
		Last Modified: Tue, 12 Nov 2024 08:40:30 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.1` - unknown; unknown

```console
$ docker pull registry@sha256:e6d34aa17920447797633f97b38602ed63c855ee99067ee0d57591dba728426f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 KB (269916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a6c69a807be921d510559ecd4d4372390a2a1b28cbf130b05b40c1780dd9b8`

```dockerfile
```

-	Layers:
	-	`sha256:d2f4b04eb9fe97f1a9ba4502167ece16509ddf6b73b93eb44c44d221dd612a4e`  
		Last Modified: Tue, 12 Nov 2024 08:40:30 GMT  
		Size: 256.4 KB (256427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb2155deaa072ba0a07b944909d0f9025371226f1cd75525224f77b5858ee7d7`  
		Last Modified: Tue, 12 Nov 2024 08:40:30 GMT  
		Size: 13.5 KB (13489 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:latest`

```console
$ docker pull registry@sha256:8fbc5829dfb333ec2bc704681b6988ab4137dfa0976ee3395e8cf7c2ee150aaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:d252b0c9a9409bb1e10a98a6b79d8f2a082284a113bc33f49121bb2fb0797cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10114147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18a86d35e983225b84aae3bb15c84bd9e47506dd0102975c0ed97958703bb73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb0aa443e23aedd28f0818f7a18de9911383d0b9b621bc448070ded1d6c81c3`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 293.4 KB (293379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813676e291ef88d6de121b9a67d4b546585c87f2b89df39d4fd14ba984cd655f`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2fb7dcec6119c150b59df0550dc646f6a45351470a7b74f0a904df40418a12`  
		Last Modified: Tue, 12 Nov 2024 02:37:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916205650bfe545ec2ac378e84f53759e0c977a77e583f0525e05cf3c8923df5`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:ef807d6ab3ae145cb40e6bc86fbd8de0fb6f4c6726ac88e619634da80dd35994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 KB (193072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e7ad24d9321d0ba3df236bcc6d5bf0a26dc6b4069c58745f6d491db169526b`

```dockerfile
```

-	Layers:
	-	`sha256:547ee2ce16efcc56c2f70e31f7327b246f129ae9e0e0f5393b19da960f910466`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 179.0 KB (179007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e019b81fd4a44bcc35582450d9aeddbdb46be2e2b6e0e5bd6cbe0dcc431d8b`  
		Last Modified: Tue, 12 Nov 2024 02:37:05 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:8351e958c42f9de2b77889506fae68712813fb6bc5f4e1579cf103bec35d41b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9477718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646ed268fea06904233caf5921a317743a80856db79e456db3956b70cc1a7b1b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-armhf.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:1ce61877166753d951080511a4649a7a9674d00fdd71569057a7f3099f39e6d8`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.2 MB (3158999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b739e776fe9e57644b5e4e99c00c4dbb4a039c894137288a095e5adcc3f78d8`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 294.0 KB (294026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5afee98ad80b18cdcc1e4f610c4b5f499b6c55c68ea75a4743e1e680fa910f4`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 6.0 MB (6024109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7f5e00a1807cf3e9f780608fcb4b45baf5e9735de16505b91749f287e31298`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adbb8c5936d65b71c7da2c2cabe8705bd496d982f440619bbe8c594d5c3f02d`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:2d1adb226ba38d47f5571423f8a72ab46d1e47a64a2274c699f648077cb956dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88f40fc59ce3d885eed54f4550aa108d5a9a860953d6fa19396d6bb55174da9`

```dockerfile
```

-	Layers:
	-	`sha256:5c26b5cde765c90b744538bf4a6ca95d05a2fb38fd9029fe5688ec806b0f1c18`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 13.9 KB (13939 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:a35141fa557e56d01aaca3b4a6dd7bbd5a1514e1398d4df026803d536a8ff981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9222062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbfc84ca3886ce8e641b5fe1b3bb8f500bd61b6b0d74420780069e9d63af0b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:6a6f0b0819f0c6585d2f9ef4edf9dc22a3f7ee9cba3de0b83dffb8f2a14dc3f3 in / 
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:9747154b8e1c5a1d049032763040bd9a6319da995da6517c17ab2d18257f0aff`  
		Last Modified: Fri, 06 Sep 2024 22:08:45 GMT  
		Size: 2.9 MB (2911364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d12bbe20fd347eff00df815b9d08c22b4a53c1fdd063f10d2a9bed89d54341`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 292.9 KB (292902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b5204efc15665e2e28441b9823b61d33ef1311df237dc837a6fd2548824f6f`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 6.0 MB (6017211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f7526059fabbb222965febd50dfb4a96970304d28e8a790b2956d7c6a29b0`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbbb78297f7d059ce8a37e1aba0a85d9870d3ac98bf2f67147162160bf1b54a`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:9a63dc1083c69a80d388e3f972c8eb6654c773633d4cf28ec8f8f1421ba37f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 KB (192752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9a2ffdc404ccb2cca80e53fc36fcd9c3641583898ec0e09d72fef675ff2beb`

```dockerfile
```

-	Layers:
	-	`sha256:b6b056e660bb162a61a44677ef9c31e908db42c4b89113707ec5900b2aba98f7`  
		Last Modified: Sat, 07 Sep 2024 12:43:51 GMT  
		Size: 178.8 KB (178831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76ef550ca1476a68f6d3d5e6987341665199a439793a97d323cba4fad15115f2`  
		Last Modified: Sat, 07 Sep 2024 12:43:50 GMT  
		Size: 13.9 KB (13921 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:1ef66c49c952ab0d20c905634d50d3a0da70133b0cdb52732a30a0fd89f01a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6adc34955df9f22da1fdc0474dcbab66dfce57ded89499201125f7dc1b9924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe29ef241d9fe87b99b77f4d96972773b3ae04f1a46c6fea0e0a60800f5f1e1`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 295.8 KB (295832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2787542bdb41f6b8315204be8ea01cb7ff82d9e6de97e9283e8af8dc6ce650e`  
		Last Modified: Tue, 12 Nov 2024 10:28:26 GMT  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b69fee0ac896543d4936d9c57aea16e665df781ec13ec5257f8bea258da7c79`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2de197705d02128cc248e6540d752209fe9ed73a32bfb6b19947205030524`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:bbf9ae6a42e4d8aef2759420301cfcc7ed642ba200ae3bf030fd5fdb9d0d2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8bd06db3380d6a4af9f2d942917235c0df5b1a02aec67120ee470ae2e11a94`

```dockerfile
```

-	Layers:
	-	`sha256:1b1f1a3aa2b9f06c429988bbdfa0c781210c0d81d6befa0769051742b9607830`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 179.1 KB (179063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a601ce5a2c5491c5fd401d93594ecbf76515407f52ce37185f82be3efee56e04`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:86cdf44fa43a89e6031fc50e516d886c0b257f9f8463548218f7aa0cddca35a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe03a1f8a043cc0d142b1dbfc0701eb12d5888e6714d95ef5de3ee3f66c3637`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-ppc64le.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bf19dcb5e2f7e7518032e1f3abc91f7a0f014fc0f3a03de278aca2c9a523ea4f`  
		Last Modified: Tue, 12 Nov 2024 00:56:06 GMT  
		Size: 3.4 MB (3358858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3792e3246e50751fd99db95bd81487f4ff267e527d2bdd744a8f15002029e84b`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 296.2 KB (296245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4725d46af85c7a6abba2419cef1cd0a36956cf13a020d059ba8751a3a0687006`  
		Last Modified: Tue, 12 Nov 2024 08:06:05 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6f196c518d25b0537d6b92276855a0f837b6f99bc09e9cd2854e83070c872`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6030f6d937516639db015c42c56128b1c45f80405aa31d885d4e91fc8cd0ea17`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:63ebe77f6c587302b3a687db1d46b6b9e8b5d89b573cfc083d1f9dad199991b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 KB (191198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e17de964dc185bfd1b49f65e7621e00c8c3a999513e31042bd22d6f293d26`

```dockerfile
```

-	Layers:
	-	`sha256:191655aad642e846fe9649b077d09cf1d11d1be5742cefe8be2036f8ceafe72f`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 177.1 KB (177087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47532ea0bac7cfc58e078cb792bdb9e1222186b96f8de6519bd95c04af4441b9`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:cad4fdf4a03376ba0904fafcb75e16e3468c10f61e3c64a4cfbb372470c8b891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7cccb184b781c20bdbb9ceff63cafb03db8074fdc32bac40da22617b729bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-s390x.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2cf6287c29b40fb867eb63db5d7189724563e69538ef303e15274f8139042129`  
		Last Modified: Tue, 12 Nov 2024 00:56:53 GMT  
		Size: 3.2 MB (3230439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149be30168d1b1aa8ec6b23c36dcdc39c2b2dcd978c5e0a2d8ca86109a0df7a`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 293.9 KB (293899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ded3165ca2acf8ea3ca820d45d88d54ade5de9f1264cc65acbe94b26d0b26`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878ae226c4b32247c8b552259cd2ff67e2c68b8c6dfe9af0b0785d28d04a9618`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277269a6b2649ecc19571438083237ee6b8b605bcb79eb5d2de467a0ab86a175`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:1c55fb5b8a1b682c0cb9ca173aa7fd36a7a8a0686c87592d298c085ba1bf31c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 KB (191118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8431cec168c6e8aeb1395b10dad52b6f9cdcadef36d4c1b5a36532ee574595ad`

```dockerfile
```

-	Layers:
	-	`sha256:7068d24c38f441b8c1a3dca81bc616b32e4c6eea0489aa2e68837a2b1d02973c`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 177.1 KB (177053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5953f2e3297796f4051786b247167696c4fdc409fca54425806f0ac4df56219`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json
