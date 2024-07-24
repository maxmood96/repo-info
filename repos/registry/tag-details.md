<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.3`](#registry283)
-	[`registry:3.0.0-beta.1`](#registry300-beta1)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:12120425f07de11a1b899e418d4b0ea174c8d4d572d45bdb640f93bc7ca06a3d
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
$ docker pull registry@sha256:5d4d001e01c8543f233d392f5519deb0d299ca89447484dab98bbd957e18c2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10113381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb4d990433561d75e90855471b1c7f095c5d54dcb731b924a74506fabcaa800`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:5851aef23205a072ef361dd412a73a39a1ada75e19a207a392bb7ec9b8556e11 in / 
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
	-	`sha256:930bdd4d222e2e63c22bd9e88d29b3c5ddd3d8a9d8fb93cf8324f4e7b9577cfb`  
		Last Modified: Mon, 22 Jul 2024 22:27:34 GMT  
		Size: 3.4 MB (3415640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15309931e0556668bfc0378bdb86325603fdeb91278a3f77250a064b0e20a15`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 293.4 KB (293366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6263fb9c821f06a8cda8e1ccd5a487d949443dac33ed1c7d0421dc5bb0d4a211`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 6.4 MB (6403791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c1d3af387238f595cc32803a1b5b7332b826ce3460a5352a39473a5ee81f80`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37b1bf6a96f6fcb5ac2b9a981a0648dbe58720ef98db756a79dbed55488d211`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:861118141af4232f68902223c734cc9ea43822d46ddba9d91bf01caf01d44ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 KB (192633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35a5a8c0c5ea4fab3741720ac1fc7f3dc86162f6992f63051d94dd7ef6e2ea4`

```dockerfile
```

-	Layers:
	-	`sha256:9039c7a7ab76ad39ee3d5fdd887ec044d5c71b63b6d90ea6b11e3cb6b6610ca3`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 178.8 KB (178795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8de6becd02cdc8d74a809a788d7a42cea42225a40976e6c8c9c2dec674114e`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 13.8 KB (13838 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm variant v6

```console
$ docker pull registry@sha256:92b8076f1ffbf1ea38e2e0dfa67890c72327ebd1ab156ee8d4b893d60996d462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9476789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d88146080f62dfc22140bca3c12e6021b5245db09baabe61629b88caddf363`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
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
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5518046d36ff19d8b656a858b8097f9e45ad9205d4271c7cc52698bbff9063b`  
		Last Modified: Tue, 23 Jul 2024 11:25:09 GMT  
		Size: 294.0 KB (294007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bb8b8dc61f5ec869d12dfab8f7ccc77cd8222de256906f631b4f4f07b10942`  
		Last Modified: Tue, 23 Jul 2024 11:25:10 GMT  
		Size: 6.0 MB (6024109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a270b7ce56ff87d1189b7b533adacceaa5763e5b11baa375a46cb7642ae03a`  
		Last Modified: Tue, 23 Jul 2024 11:25:09 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a5dba5d3b690f52070b16d52f6e17f9ce4e7078186a3ac094873fadcca39c6`  
		Last Modified: Tue, 23 Jul 2024 11:25:09 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:9863a40cc9351ce61689589b54525e0b80b6a18481f92c5e40a60e58c14523d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 KB (13702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bbadfc67b4e81cff85c51f40b1587c378c4f385a5b74739bb118eb5cf642f9`

```dockerfile
```

-	Layers:
	-	`sha256:d082bda09769f9d05021657636264e9bb57d9d4e0430b0954a3010f20dd605e8`  
		Last Modified: Tue, 23 Jul 2024 11:25:09 GMT  
		Size: 13.7 KB (13702 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm variant v7

```console
$ docker pull registry@sha256:8c712ba812f13afd8b71d7cb7ca4f9d8ce414a3fa9bdd429cdb5590a096efd04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9221274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06714bfea3431fd40a4b7a5f33c19ad6d197e466e59577131535546a4cdf0cd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:e34d98562020242f56e51e1e9951d3ad9195155680719f32de99163e05df489b in / 
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
	-	`sha256:7266492a54d392037b05dbb3028995d19457feab8d0c40848b4f829c51bd7f0a`  
		Last Modified: Mon, 22 Jul 2024 22:00:43 GMT  
		Size: 2.9 MB (2910564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667f20b79f7fc519aaab3171b34598cc10fe95457e6a2eb6168b5bd1f3914b6d`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 292.9 KB (292914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eade5636bd9fc4802061368e194780a5f6a473e628b771b6aa3bcdc5fe1889c8`  
		Last Modified: Wed, 24 Jul 2024 13:24:10 GMT  
		Size: 6.0 MB (6017215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72563de64f75167d1f3b03b5c1f7f5b0fa6bfd090b41a3e6bea3ec6ed777276`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1522c90b326c65d78722e232c7826fba31cfe95d96134c638deaa36562b17e`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:1d537062943da99b6f2ad214c45e9246fc745fdb644e9e597b3aae54fa91ebde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 KB (192751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f8e2157d71e3744583eee6ad35b2cc2d5c134fef0399c26c9a5a872d5423d9`

```dockerfile
```

-	Layers:
	-	`sha256:6c48fa9aebaf8b5034f65a3d849d724ea830c65c283eac545a8b706d8e1563cd`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 178.8 KB (178831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58149c29ea97ae038f37b0a4ece1138f29f816c39a4740b8229a219b079c12cc`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 13.9 KB (13920 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:458a3277b35a674da93aadc233e07df81628ac635c74b56a437eaea8dd4bbf41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9460624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fed88f43b27664b711c56480f81f083b8236ebf3b3a9ffa6a6f3d656d8a628c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
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
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939030e33bcd4e1f3ba7228b3c82f8ced59fea4e286a321037df7136005ccb51`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 295.8 KB (295812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffda26d630b8e031ef29181dd61b31cf4c050f31b7c5867277f89008dccaea6c`  
		Last Modified: Wed, 24 Jul 2024 07:14:56 GMT  
		Size: 5.8 MB (5824733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee21e12ed5c89a9d2aafa0073c66fc373535759867543c0224a3ba189a0dde84`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77771fb9c59220a267db1c323a75d431ce2627c54d7d356d0451917715489736`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:9d21e22931ef6a158fce09ec809f6d3113742568dea3f0191c687ddb2b077701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 KB (192989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0796978054c046fd9a3025d7d2eb558f6d7791b1da5e0afd46159c7017cbfe`

```dockerfile
```

-	Layers:
	-	`sha256:32d45ad5d1f9e05ecf52c3d7c56478cf503785a5099632e3295c86948a0b75b6`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 178.9 KB (178851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:153e9c87ab6322e56fb86efe6c7d70101a0954897b1ea4b3b48a6b31d8efbea5`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 14.1 KB (14138 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; ppc64le

```console
$ docker pull registry@sha256:c7d8d25752c8e4022e43a1ce4920ad2db1cb82d84f6d4c3744d67079633ed8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c56f40ac1ee2eb23bb771e3941876ee6a2cfc52ed034364bcf420bc4b619602`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:39fb75dfdfdb9dd435f3c590aab65b7ba2e1633e7fb84509706e3eeb59f2c5a5 in / 
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
	-	`sha256:248e3c27daa6f506dd6946aadf071230265e194056aefeb63e0bcddc4087e672`  
		Last Modified: Mon, 22 Jul 2024 21:27:13 GMT  
		Size: 3.4 MB (3358632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6394177c9e344ff7690a3cfa14d52f9dba6999735706b2641835fc6ee1222f7`  
		Last Modified: Wed, 24 Jul 2024 10:26:00 GMT  
		Size: 296.2 KB (296240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b12f807ee69a6ccb35839d4d3b3f3a60db046615812d84922223a0252edbcba`  
		Last Modified: Wed, 24 Jul 2024 10:26:00 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863361136815fcf688b3ea38ba06b28e4d77e8c1d75725e4917464963fb6d358`  
		Last Modified: Wed, 24 Jul 2024 10:25:59 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7132a55dbd15ab7d88188d6b73954b4f062acc8a19b01c7094fb0adc50e01951`  
		Last Modified: Wed, 24 Jul 2024 10:26:00 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:1c236b34d330ad833cb193f8b1c5ede23879528bcc9ba4137cf2f440c7a2da8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 KB (190753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8877ef6706805e44a0d640a743a6ce2c4918220460a3cbe5aaf64981c5766d7d`

```dockerfile
```

-	Layers:
	-	`sha256:aecef5d31e88f0c84ddac5e5f5a928abf8a1fbf8a4326d55dc292939fdc3dda6`  
		Last Modified: Wed, 24 Jul 2024 10:26:00 GMT  
		Size: 176.9 KB (176875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2fd6a7ec96db8e46171cf90ae5095d1d5dfefe00eab4b074ba8b50ff6c7232`  
		Last Modified: Wed, 24 Jul 2024 10:25:59 GMT  
		Size: 13.9 KB (13878 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; s390x

```console
$ docker pull registry@sha256:d5ab0c6336d8ffd0d0256963a040f13a77e28c6eaf7cd6fc7a6bbfc8ceef6e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2659cdacdb8c90c4b6b9f9f7ea5484be38ca34e0356811cd276eaab8d1f9e6d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:4289ff643f8649c055647843814da70f7ba2881d5fbdc6e3ece0c5b13f273fc9 in / 
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
	-	`sha256:ac5a7f502af5c00165b80407657a44a5d5f8b8b3f5f6a3c0ea73bcc6500f3466`  
		Last Modified: Mon, 22 Jul 2024 21:51:22 GMT  
		Size: 3.2 MB (3229892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bb5ecb2ec65f9e45bd14592a8d7ee2b7ec69a0b59a1b9e3393ffd86bb10843`  
		Last Modified: Wed, 24 Jul 2024 09:02:16 GMT  
		Size: 293.9 KB (293882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d95d6f4f1abbbb9d16cdd882d4e5cde73f344996a618649f78f2da6853d8f5b`  
		Last Modified: Wed, 24 Jul 2024 09:02:16 GMT  
		Size: 6.2 MB (6160048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75f26bcb42d67d49f831ad985d4885407d7e4a5c12186a12bb7ec873526e5af`  
		Last Modified: Wed, 24 Jul 2024 09:02:15 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee220608527ae8863cacebaf4dbeafcb67643101fac836a2e60d0aa2dcfcb04`  
		Last Modified: Wed, 24 Jul 2024 09:02:16 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:4bb9af01b3fef7823571ba6ad5083b8d096db618114b014be09b7de33c6a3295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 KB (190679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4878eb828b111bc6280975769caee92fdda38ddef227768f4f95e7e79069832`

```dockerfile
```

-	Layers:
	-	`sha256:472ed8d71da851e2e9bc9da0f2335868e1638febb3f6c5e5393d2102b9323542`  
		Last Modified: Wed, 24 Jul 2024 09:02:16 GMT  
		Size: 176.8 KB (176841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf47d9a4a6005592214bb2fd95b9df17d6264725f155cb2d7bd26620547f91ca`  
		Last Modified: Wed, 24 Jul 2024 09:02:15 GMT  
		Size: 13.8 KB (13838 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8`

```console
$ docker pull registry@sha256:12120425f07de11a1b899e418d4b0ea174c8d4d572d45bdb640f93bc7ca06a3d
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
$ docker pull registry@sha256:5d4d001e01c8543f233d392f5519deb0d299ca89447484dab98bbd957e18c2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10113381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb4d990433561d75e90855471b1c7f095c5d54dcb731b924a74506fabcaa800`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:5851aef23205a072ef361dd412a73a39a1ada75e19a207a392bb7ec9b8556e11 in / 
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
	-	`sha256:930bdd4d222e2e63c22bd9e88d29b3c5ddd3d8a9d8fb93cf8324f4e7b9577cfb`  
		Last Modified: Mon, 22 Jul 2024 22:27:34 GMT  
		Size: 3.4 MB (3415640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15309931e0556668bfc0378bdb86325603fdeb91278a3f77250a064b0e20a15`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 293.4 KB (293366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6263fb9c821f06a8cda8e1ccd5a487d949443dac33ed1c7d0421dc5bb0d4a211`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 6.4 MB (6403791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c1d3af387238f595cc32803a1b5b7332b826ce3460a5352a39473a5ee81f80`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37b1bf6a96f6fcb5ac2b9a981a0648dbe58720ef98db756a79dbed55488d211`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:861118141af4232f68902223c734cc9ea43822d46ddba9d91bf01caf01d44ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 KB (192633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35a5a8c0c5ea4fab3741720ac1fc7f3dc86162f6992f63051d94dd7ef6e2ea4`

```dockerfile
```

-	Layers:
	-	`sha256:9039c7a7ab76ad39ee3d5fdd887ec044d5c71b63b6d90ea6b11e3cb6b6610ca3`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 178.8 KB (178795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8de6becd02cdc8d74a809a788d7a42cea42225a40976e6c8c9c2dec674114e`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 13.8 KB (13838 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm variant v6

```console
$ docker pull registry@sha256:92b8076f1ffbf1ea38e2e0dfa67890c72327ebd1ab156ee8d4b893d60996d462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9476789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d88146080f62dfc22140bca3c12e6021b5245db09baabe61629b88caddf363`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
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
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5518046d36ff19d8b656a858b8097f9e45ad9205d4271c7cc52698bbff9063b`  
		Last Modified: Tue, 23 Jul 2024 11:25:09 GMT  
		Size: 294.0 KB (294007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bb8b8dc61f5ec869d12dfab8f7ccc77cd8222de256906f631b4f4f07b10942`  
		Last Modified: Tue, 23 Jul 2024 11:25:10 GMT  
		Size: 6.0 MB (6024109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a270b7ce56ff87d1189b7b533adacceaa5763e5b11baa375a46cb7642ae03a`  
		Last Modified: Tue, 23 Jul 2024 11:25:09 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a5dba5d3b690f52070b16d52f6e17f9ce4e7078186a3ac094873fadcca39c6`  
		Last Modified: Tue, 23 Jul 2024 11:25:09 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:9863a40cc9351ce61689589b54525e0b80b6a18481f92c5e40a60e58c14523d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 KB (13702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bbadfc67b4e81cff85c51f40b1587c378c4f385a5b74739bb118eb5cf642f9`

```dockerfile
```

-	Layers:
	-	`sha256:d082bda09769f9d05021657636264e9bb57d9d4e0430b0954a3010f20dd605e8`  
		Last Modified: Tue, 23 Jul 2024 11:25:09 GMT  
		Size: 13.7 KB (13702 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm variant v7

```console
$ docker pull registry@sha256:8c712ba812f13afd8b71d7cb7ca4f9d8ce414a3fa9bdd429cdb5590a096efd04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9221274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06714bfea3431fd40a4b7a5f33c19ad6d197e466e59577131535546a4cdf0cd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:e34d98562020242f56e51e1e9951d3ad9195155680719f32de99163e05df489b in / 
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
	-	`sha256:7266492a54d392037b05dbb3028995d19457feab8d0c40848b4f829c51bd7f0a`  
		Last Modified: Mon, 22 Jul 2024 22:00:43 GMT  
		Size: 2.9 MB (2910564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667f20b79f7fc519aaab3171b34598cc10fe95457e6a2eb6168b5bd1f3914b6d`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 292.9 KB (292914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eade5636bd9fc4802061368e194780a5f6a473e628b771b6aa3bcdc5fe1889c8`  
		Last Modified: Wed, 24 Jul 2024 13:24:10 GMT  
		Size: 6.0 MB (6017215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72563de64f75167d1f3b03b5c1f7f5b0fa6bfd090b41a3e6bea3ec6ed777276`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1522c90b326c65d78722e232c7826fba31cfe95d96134c638deaa36562b17e`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:1d537062943da99b6f2ad214c45e9246fc745fdb644e9e597b3aae54fa91ebde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 KB (192751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f8e2157d71e3744583eee6ad35b2cc2d5c134fef0399c26c9a5a872d5423d9`

```dockerfile
```

-	Layers:
	-	`sha256:6c48fa9aebaf8b5034f65a3d849d724ea830c65c283eac545a8b706d8e1563cd`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 178.8 KB (178831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58149c29ea97ae038f37b0a4ece1138f29f816c39a4740b8229a219b079c12cc`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 13.9 KB (13920 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:458a3277b35a674da93aadc233e07df81628ac635c74b56a437eaea8dd4bbf41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9460624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fed88f43b27664b711c56480f81f083b8236ebf3b3a9ffa6a6f3d656d8a628c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
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
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939030e33bcd4e1f3ba7228b3c82f8ced59fea4e286a321037df7136005ccb51`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 295.8 KB (295812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffda26d630b8e031ef29181dd61b31cf4c050f31b7c5867277f89008dccaea6c`  
		Last Modified: Wed, 24 Jul 2024 07:14:56 GMT  
		Size: 5.8 MB (5824733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee21e12ed5c89a9d2aafa0073c66fc373535759867543c0224a3ba189a0dde84`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77771fb9c59220a267db1c323a75d431ce2627c54d7d356d0451917715489736`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:9d21e22931ef6a158fce09ec809f6d3113742568dea3f0191c687ddb2b077701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 KB (192989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0796978054c046fd9a3025d7d2eb558f6d7791b1da5e0afd46159c7017cbfe`

```dockerfile
```

-	Layers:
	-	`sha256:32d45ad5d1f9e05ecf52c3d7c56478cf503785a5099632e3295c86948a0b75b6`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 178.9 KB (178851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:153e9c87ab6322e56fb86efe6c7d70101a0954897b1ea4b3b48a6b31d8efbea5`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 14.1 KB (14138 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; ppc64le

```console
$ docker pull registry@sha256:c7d8d25752c8e4022e43a1ce4920ad2db1cb82d84f6d4c3744d67079633ed8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c56f40ac1ee2eb23bb771e3941876ee6a2cfc52ed034364bcf420bc4b619602`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:39fb75dfdfdb9dd435f3c590aab65b7ba2e1633e7fb84509706e3eeb59f2c5a5 in / 
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
	-	`sha256:248e3c27daa6f506dd6946aadf071230265e194056aefeb63e0bcddc4087e672`  
		Last Modified: Mon, 22 Jul 2024 21:27:13 GMT  
		Size: 3.4 MB (3358632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6394177c9e344ff7690a3cfa14d52f9dba6999735706b2641835fc6ee1222f7`  
		Last Modified: Wed, 24 Jul 2024 10:26:00 GMT  
		Size: 296.2 KB (296240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b12f807ee69a6ccb35839d4d3b3f3a60db046615812d84922223a0252edbcba`  
		Last Modified: Wed, 24 Jul 2024 10:26:00 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863361136815fcf688b3ea38ba06b28e4d77e8c1d75725e4917464963fb6d358`  
		Last Modified: Wed, 24 Jul 2024 10:25:59 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7132a55dbd15ab7d88188d6b73954b4f062acc8a19b01c7094fb0adc50e01951`  
		Last Modified: Wed, 24 Jul 2024 10:26:00 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:1c236b34d330ad833cb193f8b1c5ede23879528bcc9ba4137cf2f440c7a2da8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 KB (190753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8877ef6706805e44a0d640a743a6ce2c4918220460a3cbe5aaf64981c5766d7d`

```dockerfile
```

-	Layers:
	-	`sha256:aecef5d31e88f0c84ddac5e5f5a928abf8a1fbf8a4326d55dc292939fdc3dda6`  
		Last Modified: Wed, 24 Jul 2024 10:26:00 GMT  
		Size: 176.9 KB (176875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2fd6a7ec96db8e46171cf90ae5095d1d5dfefe00eab4b074ba8b50ff6c7232`  
		Last Modified: Wed, 24 Jul 2024 10:25:59 GMT  
		Size: 13.9 KB (13878 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; s390x

```console
$ docker pull registry@sha256:d5ab0c6336d8ffd0d0256963a040f13a77e28c6eaf7cd6fc7a6bbfc8ceef6e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2659cdacdb8c90c4b6b9f9f7ea5484be38ca34e0356811cd276eaab8d1f9e6d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:4289ff643f8649c055647843814da70f7ba2881d5fbdc6e3ece0c5b13f273fc9 in / 
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
	-	`sha256:ac5a7f502af5c00165b80407657a44a5d5f8b8b3f5f6a3c0ea73bcc6500f3466`  
		Last Modified: Mon, 22 Jul 2024 21:51:22 GMT  
		Size: 3.2 MB (3229892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bb5ecb2ec65f9e45bd14592a8d7ee2b7ec69a0b59a1b9e3393ffd86bb10843`  
		Last Modified: Wed, 24 Jul 2024 09:02:16 GMT  
		Size: 293.9 KB (293882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d95d6f4f1abbbb9d16cdd882d4e5cde73f344996a618649f78f2da6853d8f5b`  
		Last Modified: Wed, 24 Jul 2024 09:02:16 GMT  
		Size: 6.2 MB (6160048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75f26bcb42d67d49f831ad985d4885407d7e4a5c12186a12bb7ec873526e5af`  
		Last Modified: Wed, 24 Jul 2024 09:02:15 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee220608527ae8863cacebaf4dbeafcb67643101fac836a2e60d0aa2dcfcb04`  
		Last Modified: Wed, 24 Jul 2024 09:02:16 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:4bb9af01b3fef7823571ba6ad5083b8d096db618114b014be09b7de33c6a3295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 KB (190679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4878eb828b111bc6280975769caee92fdda38ddef227768f4f95e7e79069832`

```dockerfile
```

-	Layers:
	-	`sha256:472ed8d71da851e2e9bc9da0f2335868e1638febb3f6c5e5393d2102b9323542`  
		Last Modified: Wed, 24 Jul 2024 09:02:16 GMT  
		Size: 176.8 KB (176841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf47d9a4a6005592214bb2fd95b9df17d6264725f155cb2d7bd26620547f91ca`  
		Last Modified: Wed, 24 Jul 2024 09:02:15 GMT  
		Size: 13.8 KB (13838 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8.3`

```console
$ docker pull registry@sha256:12120425f07de11a1b899e418d4b0ea174c8d4d572d45bdb640f93bc7ca06a3d
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
$ docker pull registry@sha256:5d4d001e01c8543f233d392f5519deb0d299ca89447484dab98bbd957e18c2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10113381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb4d990433561d75e90855471b1c7f095c5d54dcb731b924a74506fabcaa800`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:5851aef23205a072ef361dd412a73a39a1ada75e19a207a392bb7ec9b8556e11 in / 
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
	-	`sha256:930bdd4d222e2e63c22bd9e88d29b3c5ddd3d8a9d8fb93cf8324f4e7b9577cfb`  
		Last Modified: Mon, 22 Jul 2024 22:27:34 GMT  
		Size: 3.4 MB (3415640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15309931e0556668bfc0378bdb86325603fdeb91278a3f77250a064b0e20a15`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 293.4 KB (293366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6263fb9c821f06a8cda8e1ccd5a487d949443dac33ed1c7d0421dc5bb0d4a211`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 6.4 MB (6403791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c1d3af387238f595cc32803a1b5b7332b826ce3460a5352a39473a5ee81f80`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37b1bf6a96f6fcb5ac2b9a981a0648dbe58720ef98db756a79dbed55488d211`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:861118141af4232f68902223c734cc9ea43822d46ddba9d91bf01caf01d44ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 KB (192633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35a5a8c0c5ea4fab3741720ac1fc7f3dc86162f6992f63051d94dd7ef6e2ea4`

```dockerfile
```

-	Layers:
	-	`sha256:9039c7a7ab76ad39ee3d5fdd887ec044d5c71b63b6d90ea6b11e3cb6b6610ca3`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 178.8 KB (178795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8de6becd02cdc8d74a809a788d7a42cea42225a40976e6c8c9c2dec674114e`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 13.8 KB (13838 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm variant v6

```console
$ docker pull registry@sha256:92b8076f1ffbf1ea38e2e0dfa67890c72327ebd1ab156ee8d4b893d60996d462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9476789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d88146080f62dfc22140bca3c12e6021b5245db09baabe61629b88caddf363`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
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
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5518046d36ff19d8b656a858b8097f9e45ad9205d4271c7cc52698bbff9063b`  
		Last Modified: Tue, 23 Jul 2024 11:25:09 GMT  
		Size: 294.0 KB (294007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bb8b8dc61f5ec869d12dfab8f7ccc77cd8222de256906f631b4f4f07b10942`  
		Last Modified: Tue, 23 Jul 2024 11:25:10 GMT  
		Size: 6.0 MB (6024109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a270b7ce56ff87d1189b7b533adacceaa5763e5b11baa375a46cb7642ae03a`  
		Last Modified: Tue, 23 Jul 2024 11:25:09 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a5dba5d3b690f52070b16d52f6e17f9ce4e7078186a3ac094873fadcca39c6`  
		Last Modified: Tue, 23 Jul 2024 11:25:09 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:9863a40cc9351ce61689589b54525e0b80b6a18481f92c5e40a60e58c14523d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 KB (13702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bbadfc67b4e81cff85c51f40b1587c378c4f385a5b74739bb118eb5cf642f9`

```dockerfile
```

-	Layers:
	-	`sha256:d082bda09769f9d05021657636264e9bb57d9d4e0430b0954a3010f20dd605e8`  
		Last Modified: Tue, 23 Jul 2024 11:25:09 GMT  
		Size: 13.7 KB (13702 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm variant v7

```console
$ docker pull registry@sha256:8c712ba812f13afd8b71d7cb7ca4f9d8ce414a3fa9bdd429cdb5590a096efd04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9221274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06714bfea3431fd40a4b7a5f33c19ad6d197e466e59577131535546a4cdf0cd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:e34d98562020242f56e51e1e9951d3ad9195155680719f32de99163e05df489b in / 
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
	-	`sha256:7266492a54d392037b05dbb3028995d19457feab8d0c40848b4f829c51bd7f0a`  
		Last Modified: Mon, 22 Jul 2024 22:00:43 GMT  
		Size: 2.9 MB (2910564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667f20b79f7fc519aaab3171b34598cc10fe95457e6a2eb6168b5bd1f3914b6d`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 292.9 KB (292914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eade5636bd9fc4802061368e194780a5f6a473e628b771b6aa3bcdc5fe1889c8`  
		Last Modified: Wed, 24 Jul 2024 13:24:10 GMT  
		Size: 6.0 MB (6017215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72563de64f75167d1f3b03b5c1f7f5b0fa6bfd090b41a3e6bea3ec6ed777276`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1522c90b326c65d78722e232c7826fba31cfe95d96134c638deaa36562b17e`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:1d537062943da99b6f2ad214c45e9246fc745fdb644e9e597b3aae54fa91ebde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 KB (192751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f8e2157d71e3744583eee6ad35b2cc2d5c134fef0399c26c9a5a872d5423d9`

```dockerfile
```

-	Layers:
	-	`sha256:6c48fa9aebaf8b5034f65a3d849d724ea830c65c283eac545a8b706d8e1563cd`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 178.8 KB (178831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58149c29ea97ae038f37b0a4ece1138f29f816c39a4740b8229a219b079c12cc`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 13.9 KB (13920 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:458a3277b35a674da93aadc233e07df81628ac635c74b56a437eaea8dd4bbf41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9460624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fed88f43b27664b711c56480f81f083b8236ebf3b3a9ffa6a6f3d656d8a628c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
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
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939030e33bcd4e1f3ba7228b3c82f8ced59fea4e286a321037df7136005ccb51`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 295.8 KB (295812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffda26d630b8e031ef29181dd61b31cf4c050f31b7c5867277f89008dccaea6c`  
		Last Modified: Wed, 24 Jul 2024 07:14:56 GMT  
		Size: 5.8 MB (5824733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee21e12ed5c89a9d2aafa0073c66fc373535759867543c0224a3ba189a0dde84`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77771fb9c59220a267db1c323a75d431ce2627c54d7d356d0451917715489736`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:9d21e22931ef6a158fce09ec809f6d3113742568dea3f0191c687ddb2b077701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 KB (192989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0796978054c046fd9a3025d7d2eb558f6d7791b1da5e0afd46159c7017cbfe`

```dockerfile
```

-	Layers:
	-	`sha256:32d45ad5d1f9e05ecf52c3d7c56478cf503785a5099632e3295c86948a0b75b6`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 178.9 KB (178851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:153e9c87ab6322e56fb86efe6c7d70101a0954897b1ea4b3b48a6b31d8efbea5`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 14.1 KB (14138 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; ppc64le

```console
$ docker pull registry@sha256:c7d8d25752c8e4022e43a1ce4920ad2db1cb82d84f6d4c3744d67079633ed8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c56f40ac1ee2eb23bb771e3941876ee6a2cfc52ed034364bcf420bc4b619602`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:39fb75dfdfdb9dd435f3c590aab65b7ba2e1633e7fb84509706e3eeb59f2c5a5 in / 
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
	-	`sha256:248e3c27daa6f506dd6946aadf071230265e194056aefeb63e0bcddc4087e672`  
		Last Modified: Mon, 22 Jul 2024 21:27:13 GMT  
		Size: 3.4 MB (3358632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6394177c9e344ff7690a3cfa14d52f9dba6999735706b2641835fc6ee1222f7`  
		Last Modified: Wed, 24 Jul 2024 10:26:00 GMT  
		Size: 296.2 KB (296240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b12f807ee69a6ccb35839d4d3b3f3a60db046615812d84922223a0252edbcba`  
		Last Modified: Wed, 24 Jul 2024 10:26:00 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863361136815fcf688b3ea38ba06b28e4d77e8c1d75725e4917464963fb6d358`  
		Last Modified: Wed, 24 Jul 2024 10:25:59 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7132a55dbd15ab7d88188d6b73954b4f062acc8a19b01c7094fb0adc50e01951`  
		Last Modified: Wed, 24 Jul 2024 10:26:00 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:1c236b34d330ad833cb193f8b1c5ede23879528bcc9ba4137cf2f440c7a2da8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 KB (190753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8877ef6706805e44a0d640a743a6ce2c4918220460a3cbe5aaf64981c5766d7d`

```dockerfile
```

-	Layers:
	-	`sha256:aecef5d31e88f0c84ddac5e5f5a928abf8a1fbf8a4326d55dc292939fdc3dda6`  
		Last Modified: Wed, 24 Jul 2024 10:26:00 GMT  
		Size: 176.9 KB (176875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2fd6a7ec96db8e46171cf90ae5095d1d5dfefe00eab4b074ba8b50ff6c7232`  
		Last Modified: Wed, 24 Jul 2024 10:25:59 GMT  
		Size: 13.9 KB (13878 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; s390x

```console
$ docker pull registry@sha256:d5ab0c6336d8ffd0d0256963a040f13a77e28c6eaf7cd6fc7a6bbfc8ceef6e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2659cdacdb8c90c4b6b9f9f7ea5484be38ca34e0356811cd276eaab8d1f9e6d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:4289ff643f8649c055647843814da70f7ba2881d5fbdc6e3ece0c5b13f273fc9 in / 
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
	-	`sha256:ac5a7f502af5c00165b80407657a44a5d5f8b8b3f5f6a3c0ea73bcc6500f3466`  
		Last Modified: Mon, 22 Jul 2024 21:51:22 GMT  
		Size: 3.2 MB (3229892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bb5ecb2ec65f9e45bd14592a8d7ee2b7ec69a0b59a1b9e3393ffd86bb10843`  
		Last Modified: Wed, 24 Jul 2024 09:02:16 GMT  
		Size: 293.9 KB (293882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d95d6f4f1abbbb9d16cdd882d4e5cde73f344996a618649f78f2da6853d8f5b`  
		Last Modified: Wed, 24 Jul 2024 09:02:16 GMT  
		Size: 6.2 MB (6160048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75f26bcb42d67d49f831ad985d4885407d7e4a5c12186a12bb7ec873526e5af`  
		Last Modified: Wed, 24 Jul 2024 09:02:15 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee220608527ae8863cacebaf4dbeafcb67643101fac836a2e60d0aa2dcfcb04`  
		Last Modified: Wed, 24 Jul 2024 09:02:16 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:4bb9af01b3fef7823571ba6ad5083b8d096db618114b014be09b7de33c6a3295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 KB (190679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4878eb828b111bc6280975769caee92fdda38ddef227768f4f95e7e79069832`

```dockerfile
```

-	Layers:
	-	`sha256:472ed8d71da851e2e9bc9da0f2335868e1638febb3f6c5e5393d2102b9323542`  
		Last Modified: Wed, 24 Jul 2024 09:02:16 GMT  
		Size: 176.8 KB (176841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf47d9a4a6005592214bb2fd95b9df17d6264725f155cb2d7bd26620547f91ca`  
		Last Modified: Wed, 24 Jul 2024 09:02:15 GMT  
		Size: 13.8 KB (13838 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:3.0.0-beta.1`

```console
$ docker pull registry@sha256:efb271da5cd037b419ba464ee9ff25cc59020d2547e0eae93df7508acefaf2f2
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

### `registry:3.0.0-beta.1` - linux; amd64

```console
$ docker pull registry@sha256:73a29bfdae377b70b04c729198b113efee10cc49cf00b0c146a1c85e4d9593cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14910121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8f7973f1a705f05c71a4b44e8d00bdfac2545c2441221e748477b45ba3ffb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 10 Jul 2024 13:39:47 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Wed, 10 Jul 2024 13:39:47 GMT
CMD ["/bin/sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
RUN set -eux; 	version='3.0.0-beta.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='96344f15da3ddbef8cf300f9642d03a2b0a7aaa0b593dfe89a9ad266c5aa4ff4' ;; 		aarch64) arch='arm64';   sha256='62e3e0c168f62ac274672446a3f6ea89ebdfedc6630e4b02d93900b7022dbe88' ;; 		armhf)   arch='armv6';   sha256='01a5373d1e05bf539a1ddf5892c3bfa7377bbc02b340f6260eb7a3c62da99897' ;; 		armv7)   arch='armv7';   sha256='fb3748b3108950ba3a0b2868f4cd2317ab308d7436944bdcd3ac62f734b68eb5' ;; 		ppc64le) arch='ppc64le'; sha256='eccd060cf2d0d801fad27994d09aa43c945629cff7664f5d27bee9698b58f2a6' ;; 		s390x)   arch='s390x';   sha256='b4c415a28c9d58453455068542e92b94b080dbbbc6e990f2360098a64756c71d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Jul 2024 13:39:47 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 10 Jul 2024 13:39:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6648d15f1619ee06d1b78b1ec2d392d2bb390974139b98ea848d74fe8dcba8`  
		Last Modified: Mon, 22 Jul 2024 23:04:16 GMT  
		Size: 290.9 KB (290886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0efad9fac0a38a074b1bcb128284d3eb41a10e6709b2b99a3d48e71377b1ef`  
		Last Modified: Mon, 22 Jul 2024 23:04:16 GMT  
		Size: 11.0 MB (10995734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ad22b7cfd23b97744aa153009c0a4e21ff6eccaf8949bde96dcc84cd77dcbe`  
		Last Modified: Mon, 22 Jul 2024 23:04:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e955d93a12729e005a37068ab05f92fef950770884a7ca5c5a0c6945ba6278`  
		Last Modified: Mon, 22 Jul 2024 23:04:16 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-beta.1` - unknown; unknown

```console
$ docker pull registry@sha256:b8d4508bc5795d7aa9ad42149976553850f4afa456f06eecec68b0d7950726f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 KB (256101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142369f342464674866594b75b3bde7430e74a6ceecb47469566ee8109ed60f6`

```dockerfile
```

-	Layers:
	-	`sha256:35932ff9bc0434be8cd8a4d75a7c19fd63b8381476873371b924425488b7685f`  
		Last Modified: Mon, 22 Jul 2024 23:04:16 GMT  
		Size: 243.1 KB (243147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19388043a8cc3e49e3e6816ce7d4eb4c7d3a6d9f74e14f8a1596edea28d3ab2c`  
		Last Modified: Mon, 22 Jul 2024 23:04:15 GMT  
		Size: 13.0 KB (12954 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-beta.1` - linux; arm variant v6

```console
$ docker pull registry@sha256:2186a4b0b1ce577a235fd3e7b2ef0ab729f0df7b07e2d0bf37a6ea9235d5251b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13991936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114618e6caedf0cd5ede5e806a6841833f1ec56070e9b97f61325d7cf9aa0483`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 10 Jul 2024 13:39:47 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Wed, 10 Jul 2024 13:39:47 GMT
CMD ["/bin/sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
RUN set -eux; 	version='3.0.0-beta.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='96344f15da3ddbef8cf300f9642d03a2b0a7aaa0b593dfe89a9ad266c5aa4ff4' ;; 		aarch64) arch='arm64';   sha256='62e3e0c168f62ac274672446a3f6ea89ebdfedc6630e4b02d93900b7022dbe88' ;; 		armhf)   arch='armv6';   sha256='01a5373d1e05bf539a1ddf5892c3bfa7377bbc02b340f6260eb7a3c62da99897' ;; 		armv7)   arch='armv7';   sha256='fb3748b3108950ba3a0b2868f4cd2317ab308d7436944bdcd3ac62f734b68eb5' ;; 		ppc64le) arch='ppc64le'; sha256='eccd060cf2d0d801fad27994d09aa43c945629cff7664f5d27bee9698b58f2a6' ;; 		s390x)   arch='s390x';   sha256='b4c415a28c9d58453455068542e92b94b080dbbbc6e990f2360098a64756c71d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Jul 2024 13:39:47 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 10 Jul 2024 13:39:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c7d2c9616aacde1f6889f75c0f6fdd0ec82b6c734bb4ea060d08b15c836cde`  
		Last Modified: Tue, 23 Jul 2024 11:23:45 GMT  
		Size: 291.8 KB (291771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7feea26f23263b04f2db8ad4d78727ed0d5c551b028317d88739e23c9e59f8`  
		Last Modified: Tue, 23 Jul 2024 11:23:46 GMT  
		Size: 10.3 MB (10334365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc328612ff82d081b943ead6c77de0dd1519ec7fe242ba961cbda1de12f97271`  
		Last Modified: Tue, 23 Jul 2024 11:23:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a128937fbba2717a2fb12119d5f023938b0cfa0a1eb16a644da9f6661dfa6`  
		Last Modified: Tue, 23 Jul 2024 11:23:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-beta.1` - unknown; unknown

```console
$ docker pull registry@sha256:ac57fa8cc89c33e0dcf776e0acda34aad3f3e93075b9606423835558e7248c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e538467b70703e61e448c97d6f20478215433ee546d1c04bfcd2b0bc3a288112`

```dockerfile
```

-	Layers:
	-	`sha256:67e3d07ca42e022a54b1eb95a8a1cf1cc00933316584391fad9ebc6d36f0c40e`  
		Last Modified: Tue, 23 Jul 2024 11:23:45 GMT  
		Size: 12.8 KB (12794 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-beta.1` - linux; arm variant v7

```console
$ docker pull registry@sha256:445bade4436cdde62c2dd12a7f67e2eac01b2d0a149ad1bbd44d39218bfc5b91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13714244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888fa97be68cd358a8b613975852dd6fe39904eafa5caa42dc69c3713fa865a3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 10 Jul 2024 13:39:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Wed, 10 Jul 2024 13:39:47 GMT
CMD ["/bin/sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
RUN set -eux; 	version='3.0.0-beta.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='96344f15da3ddbef8cf300f9642d03a2b0a7aaa0b593dfe89a9ad266c5aa4ff4' ;; 		aarch64) arch='arm64';   sha256='62e3e0c168f62ac274672446a3f6ea89ebdfedc6630e4b02d93900b7022dbe88' ;; 		armhf)   arch='armv6';   sha256='01a5373d1e05bf539a1ddf5892c3bfa7377bbc02b340f6260eb7a3c62da99897' ;; 		armv7)   arch='armv7';   sha256='fb3748b3108950ba3a0b2868f4cd2317ab308d7436944bdcd3ac62f734b68eb5' ;; 		ppc64le) arch='ppc64le'; sha256='eccd060cf2d0d801fad27994d09aa43c945629cff7664f5d27bee9698b58f2a6' ;; 		s390x)   arch='s390x';   sha256='b4c415a28c9d58453455068542e92b94b080dbbbc6e990f2360098a64756c71d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Jul 2024 13:39:47 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 10 Jul 2024 13:39:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca84a11d54b701c6be97a67ac2a525b40a340c6bd21d283e82380d3f7d9afb6`  
		Last Modified: Wed, 24 Jul 2024 13:23:46 GMT  
		Size: 291.0 KB (290960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59f6719286c657214784bc26f85a13b876e892432aa759cb0ffb0583172d4d7`  
		Last Modified: Wed, 24 Jul 2024 13:23:47 GMT  
		Size: 10.3 MB (10327715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a4f5f2a38f72026a27d6c30f09a8621c08eea14b13837d97d3ad5bf7e05d9b`  
		Last Modified: Wed, 24 Jul 2024 13:23:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a158e65e43b4a5d7b7f7d6a9b948452dcd37ac10d8f7d0555ac1265ebeb98fbb`  
		Last Modified: Wed, 24 Jul 2024 13:23:46 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-beta.1` - unknown; unknown

```console
$ docker pull registry@sha256:28e1cbfde99ce339bb687cdcf52618bb0428f8751d7b181b060edeecd792dcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 KB (256172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b086bd86871f9cd808a536307293d710d2b992b8fd708427a55785cc2639783b`

```dockerfile
```

-	Layers:
	-	`sha256:1507a4a8689863f3442d75696e7ac8876c3822951c3cd934459a040159fd3568`  
		Last Modified: Wed, 24 Jul 2024 13:23:46 GMT  
		Size: 243.2 KB (243159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921c3636ed471268c43a1d966526e940da7e8bfbf1416d855eff371318d09020`  
		Last Modified: Wed, 24 Jul 2024 13:23:46 GMT  
		Size: 13.0 KB (13013 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-beta.1` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:2b2e9788cdbfb81966c7856ab572dc8b1389ce14b1e2760ef1da3e8b743ec427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14546537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1d01f3282a696127713003ac2c23f4906d8e43c50023a0bf3f9a75aeb941dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 10 Jul 2024 13:39:47 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Wed, 10 Jul 2024 13:39:47 GMT
CMD ["/bin/sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
RUN set -eux; 	version='3.0.0-beta.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='96344f15da3ddbef8cf300f9642d03a2b0a7aaa0b593dfe89a9ad266c5aa4ff4' ;; 		aarch64) arch='arm64';   sha256='62e3e0c168f62ac274672446a3f6ea89ebdfedc6630e4b02d93900b7022dbe88' ;; 		armhf)   arch='armv6';   sha256='01a5373d1e05bf539a1ddf5892c3bfa7377bbc02b340f6260eb7a3c62da99897' ;; 		armv7)   arch='armv7';   sha256='fb3748b3108950ba3a0b2868f4cd2317ab308d7436944bdcd3ac62f734b68eb5' ;; 		ppc64le) arch='ppc64le'; sha256='eccd060cf2d0d801fad27994d09aa43c945629cff7664f5d27bee9698b58f2a6' ;; 		s390x)   arch='s390x';   sha256='b4c415a28c9d58453455068542e92b94b080dbbbc6e990f2360098a64756c71d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Jul 2024 13:39:47 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 10 Jul 2024 13:39:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5080a8437b1abab2c4dc62b723df2744a2fe2e938de969dff4d6d45420312006`  
		Last Modified: Wed, 24 Jul 2024 07:14:35 GMT  
		Size: 293.5 KB (293526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31a457289301cda003cb26b1c0cf89b1389ac996e0a4ac09f394fb51d1fcb1f`  
		Last Modified: Wed, 24 Jul 2024 07:14:36 GMT  
		Size: 10.2 MB (10165466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a9ecacc2d81d737f636cbc0d3563178660b6e0da3e6de16cf792b89405ae52`  
		Last Modified: Wed, 24 Jul 2024 07:14:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64552236258daf771b89bb570b28207fa04c2613b0cc1e6be9db0d6d17d728b0`  
		Last Modified: Wed, 24 Jul 2024 07:14:35 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-beta.1` - unknown; unknown

```console
$ docker pull registry@sha256:a210fa976f49aab3a116f7411f1617a4465dbb19f0b7173052ec76baa96acc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 KB (256384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:315d0b6f03771033ad00606ab2f35033a9c747668fd38c347aa40e475e431309`

```dockerfile
```

-	Layers:
	-	`sha256:c9dc647de767405f87c49d0c2e9ae549f542faedf9b6ab0b445d23dc19e454df`  
		Last Modified: Wed, 24 Jul 2024 07:14:35 GMT  
		Size: 243.2 KB (243167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8f07122fbde42c289068751fc24d05d6c6641203149674582c01e9e0aa8b6ef`  
		Last Modified: Wed, 24 Jul 2024 07:14:35 GMT  
		Size: 13.2 KB (13217 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-beta.1` - linux; ppc64le

```console
$ docker pull registry@sha256:88166ec28de0abdbcaa6883579c38add38a6fb13f2e1d3a3deaeb424312b6454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13787043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96cf5a598b7f818f28e41bc113585cc36fa645d12f89fe1724d680c958ab8aad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 10 Jul 2024 13:39:47 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Wed, 10 Jul 2024 13:39:47 GMT
CMD ["/bin/sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
RUN set -eux; 	version='3.0.0-beta.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='96344f15da3ddbef8cf300f9642d03a2b0a7aaa0b593dfe89a9ad266c5aa4ff4' ;; 		aarch64) arch='arm64';   sha256='62e3e0c168f62ac274672446a3f6ea89ebdfedc6630e4b02d93900b7022dbe88' ;; 		armhf)   arch='armv6';   sha256='01a5373d1e05bf539a1ddf5892c3bfa7377bbc02b340f6260eb7a3c62da99897' ;; 		armv7)   arch='armv7';   sha256='fb3748b3108950ba3a0b2868f4cd2317ab308d7436944bdcd3ac62f734b68eb5' ;; 		ppc64le) arch='ppc64le'; sha256='eccd060cf2d0d801fad27994d09aa43c945629cff7664f5d27bee9698b58f2a6' ;; 		s390x)   arch='s390x';   sha256='b4c415a28c9d58453455068542e92b94b080dbbbc6e990f2360098a64756c71d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Jul 2024 13:39:47 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 10 Jul 2024 13:39:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384b08f89f73d5e051cad7d20970661bf17995762f12461f9064c3de2d58bab4`  
		Last Modified: Wed, 24 Jul 2024 10:25:26 GMT  
		Size: 294.0 KB (294038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acafdab49fec7f3283aec596802358ccfb6c37271c6fb715881042246d32195`  
		Last Modified: Wed, 24 Jul 2024 10:25:26 GMT  
		Size: 9.9 MB (9920840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329d09718afa7cfd45a993ef6ad07a8adc9f296aa0dc29492e5fecaecf512859`  
		Last Modified: Wed, 24 Jul 2024 10:25:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6e22bff46f2204bac3378bbfbffc93d2d3c96562cee2e7bcc25b2600baddf0`  
		Last Modified: Wed, 24 Jul 2024 10:25:26 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-beta.1` - unknown; unknown

```console
$ docker pull registry@sha256:1068234d470b503bd91553440b4b82f20962219f8aa604d8c7cf692dbc2d77b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 KB (254182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81216abf6a39f7ea08f2a69a150f45bd0f5aab8640205ee725a4b10e2134ac03`

```dockerfile
```

-	Layers:
	-	`sha256:cb30e4e4dff75ccb3b1aca9eb6f6289457486dfe4257001023c07c291700a66e`  
		Last Modified: Wed, 24 Jul 2024 10:25:26 GMT  
		Size: 241.2 KB (241209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c5e4e93eb70cc07d83049850745acd086c2dfc06f2d5fa7d208e4011fa0b0be`  
		Last Modified: Wed, 24 Jul 2024 10:25:26 GMT  
		Size: 13.0 KB (12973 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-beta.1` - linux; s390x

```console
$ docker pull registry@sha256:aa0bd958a961ffe3ea6464963ed8aba0bf17974fd66404843bec514dfa213c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14298986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc701c2d18ba2defd34eab8c090a57ae8a374e56ff09891a4d77f9d7efeb87fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 10 Jul 2024 13:39:47 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Wed, 10 Jul 2024 13:39:47 GMT
CMD ["/bin/sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
RUN set -eux; 	version='3.0.0-beta.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='96344f15da3ddbef8cf300f9642d03a2b0a7aaa0b593dfe89a9ad266c5aa4ff4' ;; 		aarch64) arch='arm64';   sha256='62e3e0c168f62ac274672446a3f6ea89ebdfedc6630e4b02d93900b7022dbe88' ;; 		armhf)   arch='armv6';   sha256='01a5373d1e05bf539a1ddf5892c3bfa7377bbc02b340f6260eb7a3c62da99897' ;; 		armv7)   arch='armv7';   sha256='fb3748b3108950ba3a0b2868f4cd2317ab308d7436944bdcd3ac62f734b68eb5' ;; 		ppc64le) arch='ppc64le'; sha256='eccd060cf2d0d801fad27994d09aa43c945629cff7664f5d27bee9698b58f2a6' ;; 		s390x)   arch='s390x';   sha256='b4c415a28c9d58453455068542e92b94b080dbbbc6e990f2360098a64756c71d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
VOLUME [/var/lib/registry]
# Wed, 10 Jul 2024 13:39:47 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 10 Jul 2024 13:39:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 10 Jul 2024 13:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jul 2024 13:39:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263efb22488e2d2371b2aacc27cd5d2b7c1ed3fd431d7a12f2126af60aaab21`  
		Last Modified: Wed, 24 Jul 2024 09:01:32 GMT  
		Size: 291.9 KB (291896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b51d34ab7c26bbd620b8ac3cbfe936f1538a16428ae27dc76bd57cf0341a8a`  
		Last Modified: Wed, 24 Jul 2024 09:01:32 GMT  
		Size: 10.5 MB (10545413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b9975ca5f5a8eb58a04c62b85c088b0bbef8c6aa1dbe8164d3bea8b5c075dc`  
		Last Modified: Wed, 24 Jul 2024 09:01:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89c506587c4bda632fdb911e3a5b6037aa9d53b62f8fca076ecf92c0fa2974f`  
		Last Modified: Wed, 24 Jul 2024 09:01:32 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-beta.1` - unknown; unknown

```console
$ docker pull registry@sha256:b77a66f46d02f69d11e3103cdb3b42def51959495c35488a6c2a796d23c6e0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 KB (254133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf596fac8fcf369fa3d46500f97ed5bec85d2c4c2858864164fe7739aabb6e96`

```dockerfile
```

-	Layers:
	-	`sha256:550c5b9be78cee86f1db3f9f613bdaa587d8d02351057457d8d59c6f433e1ebd`  
		Last Modified: Wed, 24 Jul 2024 09:01:32 GMT  
		Size: 241.2 KB (241179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86edded56ea2ba6114afcde005bbdf7b1a217120e31a0cd04f9e732fbf086a9b`  
		Last Modified: Wed, 24 Jul 2024 09:01:31 GMT  
		Size: 13.0 KB (12954 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:latest`

```console
$ docker pull registry@sha256:12120425f07de11a1b899e418d4b0ea174c8d4d572d45bdb640f93bc7ca06a3d
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
$ docker pull registry@sha256:5d4d001e01c8543f233d392f5519deb0d299ca89447484dab98bbd957e18c2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10113381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb4d990433561d75e90855471b1c7f095c5d54dcb731b924a74506fabcaa800`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:5851aef23205a072ef361dd412a73a39a1ada75e19a207a392bb7ec9b8556e11 in / 
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
	-	`sha256:930bdd4d222e2e63c22bd9e88d29b3c5ddd3d8a9d8fb93cf8324f4e7b9577cfb`  
		Last Modified: Mon, 22 Jul 2024 22:27:34 GMT  
		Size: 3.4 MB (3415640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15309931e0556668bfc0378bdb86325603fdeb91278a3f77250a064b0e20a15`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 293.4 KB (293366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6263fb9c821f06a8cda8e1ccd5a487d949443dac33ed1c7d0421dc5bb0d4a211`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 6.4 MB (6403791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c1d3af387238f595cc32803a1b5b7332b826ce3460a5352a39473a5ee81f80`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37b1bf6a96f6fcb5ac2b9a981a0648dbe58720ef98db756a79dbed55488d211`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:861118141af4232f68902223c734cc9ea43822d46ddba9d91bf01caf01d44ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 KB (192633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35a5a8c0c5ea4fab3741720ac1fc7f3dc86162f6992f63051d94dd7ef6e2ea4`

```dockerfile
```

-	Layers:
	-	`sha256:9039c7a7ab76ad39ee3d5fdd887ec044d5c71b63b6d90ea6b11e3cb6b6610ca3`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 178.8 KB (178795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8de6becd02cdc8d74a809a788d7a42cea42225a40976e6c8c9c2dec674114e`  
		Last Modified: Mon, 22 Jul 2024 23:04:07 GMT  
		Size: 13.8 KB (13838 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:92b8076f1ffbf1ea38e2e0dfa67890c72327ebd1ab156ee8d4b893d60996d462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9476789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d88146080f62dfc22140bca3c12e6021b5245db09baabe61629b88caddf363`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:563fdf5092d9904eba8b5f0f0e881bed7eab326ea811d934e3bf5d1a2032f54d in / 
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
	-	`sha256:7dda9a44ae82b876e897d397270585fb4961cf54d8b9a6ca9cbfd5b57a7621ea`  
		Last Modified: Mon, 22 Jul 2024 21:50:01 GMT  
		Size: 3.2 MB (3158088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5518046d36ff19d8b656a858b8097f9e45ad9205d4271c7cc52698bbff9063b`  
		Last Modified: Tue, 23 Jul 2024 11:25:09 GMT  
		Size: 294.0 KB (294007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bb8b8dc61f5ec869d12dfab8f7ccc77cd8222de256906f631b4f4f07b10942`  
		Last Modified: Tue, 23 Jul 2024 11:25:10 GMT  
		Size: 6.0 MB (6024109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a270b7ce56ff87d1189b7b533adacceaa5763e5b11baa375a46cb7642ae03a`  
		Last Modified: Tue, 23 Jul 2024 11:25:09 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a5dba5d3b690f52070b16d52f6e17f9ce4e7078186a3ac094873fadcca39c6`  
		Last Modified: Tue, 23 Jul 2024 11:25:09 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:9863a40cc9351ce61689589b54525e0b80b6a18481f92c5e40a60e58c14523d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 KB (13702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bbadfc67b4e81cff85c51f40b1587c378c4f385a5b74739bb118eb5cf642f9`

```dockerfile
```

-	Layers:
	-	`sha256:d082bda09769f9d05021657636264e9bb57d9d4e0430b0954a3010f20dd605e8`  
		Last Modified: Tue, 23 Jul 2024 11:25:09 GMT  
		Size: 13.7 KB (13702 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:8c712ba812f13afd8b71d7cb7ca4f9d8ce414a3fa9bdd429cdb5590a096efd04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9221274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06714bfea3431fd40a4b7a5f33c19ad6d197e466e59577131535546a4cdf0cd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:e34d98562020242f56e51e1e9951d3ad9195155680719f32de99163e05df489b in / 
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
	-	`sha256:7266492a54d392037b05dbb3028995d19457feab8d0c40848b4f829c51bd7f0a`  
		Last Modified: Mon, 22 Jul 2024 22:00:43 GMT  
		Size: 2.9 MB (2910564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667f20b79f7fc519aaab3171b34598cc10fe95457e6a2eb6168b5bd1f3914b6d`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 292.9 KB (292914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eade5636bd9fc4802061368e194780a5f6a473e628b771b6aa3bcdc5fe1889c8`  
		Last Modified: Wed, 24 Jul 2024 13:24:10 GMT  
		Size: 6.0 MB (6017215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72563de64f75167d1f3b03b5c1f7f5b0fa6bfd090b41a3e6bea3ec6ed777276`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1522c90b326c65d78722e232c7826fba31cfe95d96134c638deaa36562b17e`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:1d537062943da99b6f2ad214c45e9246fc745fdb644e9e597b3aae54fa91ebde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 KB (192751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f8e2157d71e3744583eee6ad35b2cc2d5c134fef0399c26c9a5a872d5423d9`

```dockerfile
```

-	Layers:
	-	`sha256:6c48fa9aebaf8b5034f65a3d849d724ea830c65c283eac545a8b706d8e1563cd`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 178.8 KB (178831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58149c29ea97ae038f37b0a4ece1138f29f816c39a4740b8229a219b079c12cc`  
		Last Modified: Wed, 24 Jul 2024 13:24:09 GMT  
		Size: 13.9 KB (13920 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:458a3277b35a674da93aadc233e07df81628ac635c74b56a437eaea8dd4bbf41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9460624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fed88f43b27664b711c56480f81f083b8236ebf3b3a9ffa6a6f3d656d8a628c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
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
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939030e33bcd4e1f3ba7228b3c82f8ced59fea4e286a321037df7136005ccb51`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 295.8 KB (295812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffda26d630b8e031ef29181dd61b31cf4c050f31b7c5867277f89008dccaea6c`  
		Last Modified: Wed, 24 Jul 2024 07:14:56 GMT  
		Size: 5.8 MB (5824733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee21e12ed5c89a9d2aafa0073c66fc373535759867543c0224a3ba189a0dde84`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77771fb9c59220a267db1c323a75d431ce2627c54d7d356d0451917715489736`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:9d21e22931ef6a158fce09ec809f6d3113742568dea3f0191c687ddb2b077701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 KB (192989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0796978054c046fd9a3025d7d2eb558f6d7791b1da5e0afd46159c7017cbfe`

```dockerfile
```

-	Layers:
	-	`sha256:32d45ad5d1f9e05ecf52c3d7c56478cf503785a5099632e3295c86948a0b75b6`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 178.9 KB (178851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:153e9c87ab6322e56fb86efe6c7d70101a0954897b1ea4b3b48a6b31d8efbea5`  
		Last Modified: Wed, 24 Jul 2024 07:14:55 GMT  
		Size: 14.1 KB (14138 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:c7d8d25752c8e4022e43a1ce4920ad2db1cb82d84f6d4c3744d67079633ed8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c56f40ac1ee2eb23bb771e3941876ee6a2cfc52ed034364bcf420bc4b619602`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:39fb75dfdfdb9dd435f3c590aab65b7ba2e1633e7fb84509706e3eeb59f2c5a5 in / 
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
	-	`sha256:248e3c27daa6f506dd6946aadf071230265e194056aefeb63e0bcddc4087e672`  
		Last Modified: Mon, 22 Jul 2024 21:27:13 GMT  
		Size: 3.4 MB (3358632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6394177c9e344ff7690a3cfa14d52f9dba6999735706b2641835fc6ee1222f7`  
		Last Modified: Wed, 24 Jul 2024 10:26:00 GMT  
		Size: 296.2 KB (296240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b12f807ee69a6ccb35839d4d3b3f3a60db046615812d84922223a0252edbcba`  
		Last Modified: Wed, 24 Jul 2024 10:26:00 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863361136815fcf688b3ea38ba06b28e4d77e8c1d75725e4917464963fb6d358`  
		Last Modified: Wed, 24 Jul 2024 10:25:59 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7132a55dbd15ab7d88188d6b73954b4f062acc8a19b01c7094fb0adc50e01951`  
		Last Modified: Wed, 24 Jul 2024 10:26:00 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:1c236b34d330ad833cb193f8b1c5ede23879528bcc9ba4137cf2f440c7a2da8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 KB (190753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8877ef6706805e44a0d640a743a6ce2c4918220460a3cbe5aaf64981c5766d7d`

```dockerfile
```

-	Layers:
	-	`sha256:aecef5d31e88f0c84ddac5e5f5a928abf8a1fbf8a4326d55dc292939fdc3dda6`  
		Last Modified: Wed, 24 Jul 2024 10:26:00 GMT  
		Size: 176.9 KB (176875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2fd6a7ec96db8e46171cf90ae5095d1d5dfefe00eab4b074ba8b50ff6c7232`  
		Last Modified: Wed, 24 Jul 2024 10:25:59 GMT  
		Size: 13.9 KB (13878 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:d5ab0c6336d8ffd0d0256963a040f13a77e28c6eaf7cd6fc7a6bbfc8ceef6e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2659cdacdb8c90c4b6b9f9f7ea5484be38ca34e0356811cd276eaab8d1f9e6d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:4289ff643f8649c055647843814da70f7ba2881d5fbdc6e3ece0c5b13f273fc9 in / 
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
	-	`sha256:ac5a7f502af5c00165b80407657a44a5d5f8b8b3f5f6a3c0ea73bcc6500f3466`  
		Last Modified: Mon, 22 Jul 2024 21:51:22 GMT  
		Size: 3.2 MB (3229892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bb5ecb2ec65f9e45bd14592a8d7ee2b7ec69a0b59a1b9e3393ffd86bb10843`  
		Last Modified: Wed, 24 Jul 2024 09:02:16 GMT  
		Size: 293.9 KB (293882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d95d6f4f1abbbb9d16cdd882d4e5cde73f344996a618649f78f2da6853d8f5b`  
		Last Modified: Wed, 24 Jul 2024 09:02:16 GMT  
		Size: 6.2 MB (6160048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75f26bcb42d67d49f831ad985d4885407d7e4a5c12186a12bb7ec873526e5af`  
		Last Modified: Wed, 24 Jul 2024 09:02:15 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee220608527ae8863cacebaf4dbeafcb67643101fac836a2e60d0aa2dcfcb04`  
		Last Modified: Wed, 24 Jul 2024 09:02:16 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:4bb9af01b3fef7823571ba6ad5083b8d096db618114b014be09b7de33c6a3295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 KB (190679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4878eb828b111bc6280975769caee92fdda38ddef227768f4f95e7e79069832`

```dockerfile
```

-	Layers:
	-	`sha256:472ed8d71da851e2e9bc9da0f2335868e1638febb3f6c5e5393d2102b9323542`  
		Last Modified: Wed, 24 Jul 2024 09:02:16 GMT  
		Size: 176.8 KB (176841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf47d9a4a6005592214bb2fd95b9df17d6264725f155cb2d7bd26620547f91ca`  
		Last Modified: Wed, 24 Jul 2024 09:02:15 GMT  
		Size: 13.8 KB (13838 bytes)  
		MIME: application/vnd.in-toto+json
