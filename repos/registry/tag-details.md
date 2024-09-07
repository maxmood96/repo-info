<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.3`](#registry283)
-	[`registry:3.0.0-beta.1`](#registry300-beta1)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:2138d01b38545123ac695fd532c666c7ee0a37781358c15737297770586d11a9
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
$ docker pull registry@sha256:5e8c7f954d64eb89a98a3f84b6dd1e1f4a9cf3d25e41575dd0a96d3e3363cba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10114050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ef5b734af47dc41ff2fb442f287ee08c7da31dddb3759616a8f693f0f346a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
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
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ab09421e5ab31796387697888ea35062381139bc482bd424a44d8641207945`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 293.4 KB (293370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40960af72c1c69115fac00e5200d74c78f60acdaf51c7218166781e86b4ea9c1`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bb1dbb377ee0338b3b86dae5d6a2e5530fe03d188d552578f425be24bdf64a`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a538cc9b1ae3c5b339a8c01b77a23b3d6d28a634d05c9ec27f753389931e0552`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:7dfb23ec91fbf29941cf3d5a8be16e7555166b982b3e6544e0662811cd4d15d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 KB (192633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076f378091a9c20d30c1ac87002851f45f1b9f388dd8e769a17a80f5a49f0355`

```dockerfile
```

-	Layers:
	-	`sha256:a6009a951c3d76c9132bc57451567238636504b66bcae0b08de8f56de249cd88`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 178.8 KB (178795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccc12179a4b433c440436a1c0c56fd5b78d8430128385c97d9f112a25f184f81`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
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
$ docker pull registry@sha256:17f2b46e3f28d86aa0d051552cecaf9e09f7d0f664a80ef4745d1102f7ff2323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9cf76bb104e1d7bf59b23d4b9af832bf75736893c2fece60665bfdc73006bcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:c2dbff469fced00345f9627d1efd892f94d53dbb31a6485fa9411b2fb1b4840f in / 
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
	-	`sha256:720f3032cd1105e6311c8adee3ee0f3b6827bec2c48f1cfff486a347ad22f05c`  
		Last Modified: Fri, 06 Sep 2024 22:44:58 GMT  
		Size: 3.3 MB (3340347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d259642272e58761a700b543b776612d3c845e0c6b44ed1e0310391decbecafb`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 295.8 KB (295824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e496f3330122160bc7189304622bf8abe6a2ae218ccb0e821b2021893d48b68`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 5.8 MB (5824732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e961822193ae9a01b0dedeb124ed4268485dfaad16b6e3a3de2315601dafeeaa`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98a2db964ee0b7107b82305b8911d3f3395e05039b068f8aebff82fd57adb0e`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:149c40af501a6e96b60df39771ace01be069225a9a68758f16e22b4983839a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 KB (192989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526f372eda7cba4b0edfcd064c841e4bb19756e86a819eb949673810c7a72610`

```dockerfile
```

-	Layers:
	-	`sha256:67572e10d475c7d60d02a046567b7a8e5e5993e309fb3272515c9b042bbf4582`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 178.9 KB (178851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4124005187b1cab3478c87c0d84a7a2431ba0f1f0800238426711c35204460ed`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 14.1 KB (14138 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; ppc64le

```console
$ docker pull registry@sha256:1a5dd6584bd8161465f83b444c25bfda8da69e06fbe041fade4f1b32b3c776df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c749e4a884836945250c96e95c49968f6fa318e502278f2381e98a531c67a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:2b1a723fec64c757d924d7e1e007f92ef7f3d7e7c91198b52ccf7c47d5a4d10a in / 
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
	-	`sha256:09f69d5d2e4b62e458d29b2e4d2542a265853dd015a23f55217326820e81d7d9`  
		Last Modified: Fri, 06 Sep 2024 22:26:59 GMT  
		Size: 3.4 MB (3358817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f021a2a9854b506a06eea76cab86a36ed7f250bd508bceb7666b89053c4796f`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 296.2 KB (296243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafd9592e7a1fd1d027f54305c4e4fb5e20405b9c43009723ba04fca50d77a64`  
		Last Modified: Sat, 07 Sep 2024 11:29:35 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26273b826329a3b2a2131075a0730124bbcac966e967ca93997059bdabaa54e5`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e03ddbd617155d43db86de6cc6f17509498ad050bb00d7ed332bfb33d5e696`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:602e33f9e9fb3c76e4f743791ce778aeff73e573dc2e0ec01a337bb203a457b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 KB (190753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b822904f2f33756cbb47dbffb908b14f75a5e531ca2490395254fdfa860e226`

```dockerfile
```

-	Layers:
	-	`sha256:33f6a549437f27db6e750cfaaa06010f51b58580035b760b72ea1fb72a3da969`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 176.9 KB (176875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb8aed2a37a0588e84955cca589c4f048554636ad5f4869045c82c006d218b9d`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 13.9 KB (13878 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; s390x

```console
$ docker pull registry@sha256:b425d1e159bf0a98fa38fc40e56c65852df7d0f9240eb5e053e707513fb779ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8715c811817919d11e77f2ddb041515209d8660d7c4ba174b9fdea04a8d290`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:915212fdde86cc10e2c0038779562c7f4c2d80f238c5807ab3e6bf15c3f207ae in / 
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
	-	`sha256:e1969bec132c5668fa6607cfae829c75ec87bce5e800a6cb6454687412d3c2db`  
		Last Modified: Fri, 06 Sep 2024 22:49:09 GMT  
		Size: 3.2 MB (3230415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d61c62fb5b980e996ccef94ff2a9d02a5d8bf74ea9f207154f19e6ec47e074b`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 293.9 KB (293885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd490e06e2ae62a247359af493fe767b91aa091c5d8702b061c25d6446091713`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2056d8d717fe1c97e0ea3cadc789fe84ef61ccfceb4ed07c0bd118056015a78d`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48e631184dc020d330d4c0357a3b2b24dbb0715f7dba3c45ce008c90f4d8929`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:85772e4077bc98a05e7e47b5757faf18327329b216ba4be88a132688cfd0895d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 KB (190679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e21b280ca98e362100cecc1fa546a73b58be6a7401768b7cfceeb2f88741404`

```dockerfile
```

-	Layers:
	-	`sha256:1ffeb8bc912295bb8701cab8f24ba9f0434968cc429c8d99c9be67b8f681c4d3`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 176.8 KB (176841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b451a8f2dbf54a608c1656d3645a71e4cb398a740a2401fbdfec874074f4fa8f`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 13.8 KB (13838 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8`

```console
$ docker pull registry@sha256:2138d01b38545123ac695fd532c666c7ee0a37781358c15737297770586d11a9
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
$ docker pull registry@sha256:5e8c7f954d64eb89a98a3f84b6dd1e1f4a9cf3d25e41575dd0a96d3e3363cba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10114050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ef5b734af47dc41ff2fb442f287ee08c7da31dddb3759616a8f693f0f346a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
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
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ab09421e5ab31796387697888ea35062381139bc482bd424a44d8641207945`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 293.4 KB (293370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40960af72c1c69115fac00e5200d74c78f60acdaf51c7218166781e86b4ea9c1`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bb1dbb377ee0338b3b86dae5d6a2e5530fe03d188d552578f425be24bdf64a`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a538cc9b1ae3c5b339a8c01b77a23b3d6d28a634d05c9ec27f753389931e0552`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:7dfb23ec91fbf29941cf3d5a8be16e7555166b982b3e6544e0662811cd4d15d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 KB (192633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076f378091a9c20d30c1ac87002851f45f1b9f388dd8e769a17a80f5a49f0355`

```dockerfile
```

-	Layers:
	-	`sha256:a6009a951c3d76c9132bc57451567238636504b66bcae0b08de8f56de249cd88`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 178.8 KB (178795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccc12179a4b433c440436a1c0c56fd5b78d8430128385c97d9f112a25f184f81`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
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
$ docker pull registry@sha256:17f2b46e3f28d86aa0d051552cecaf9e09f7d0f664a80ef4745d1102f7ff2323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9cf76bb104e1d7bf59b23d4b9af832bf75736893c2fece60665bfdc73006bcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:c2dbff469fced00345f9627d1efd892f94d53dbb31a6485fa9411b2fb1b4840f in / 
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
	-	`sha256:720f3032cd1105e6311c8adee3ee0f3b6827bec2c48f1cfff486a347ad22f05c`  
		Last Modified: Fri, 06 Sep 2024 22:44:58 GMT  
		Size: 3.3 MB (3340347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d259642272e58761a700b543b776612d3c845e0c6b44ed1e0310391decbecafb`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 295.8 KB (295824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e496f3330122160bc7189304622bf8abe6a2ae218ccb0e821b2021893d48b68`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 5.8 MB (5824732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e961822193ae9a01b0dedeb124ed4268485dfaad16b6e3a3de2315601dafeeaa`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98a2db964ee0b7107b82305b8911d3f3395e05039b068f8aebff82fd57adb0e`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:149c40af501a6e96b60df39771ace01be069225a9a68758f16e22b4983839a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 KB (192989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526f372eda7cba4b0edfcd064c841e4bb19756e86a819eb949673810c7a72610`

```dockerfile
```

-	Layers:
	-	`sha256:67572e10d475c7d60d02a046567b7a8e5e5993e309fb3272515c9b042bbf4582`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 178.9 KB (178851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4124005187b1cab3478c87c0d84a7a2431ba0f1f0800238426711c35204460ed`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 14.1 KB (14138 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; ppc64le

```console
$ docker pull registry@sha256:1a5dd6584bd8161465f83b444c25bfda8da69e06fbe041fade4f1b32b3c776df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c749e4a884836945250c96e95c49968f6fa318e502278f2381e98a531c67a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:2b1a723fec64c757d924d7e1e007f92ef7f3d7e7c91198b52ccf7c47d5a4d10a in / 
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
	-	`sha256:09f69d5d2e4b62e458d29b2e4d2542a265853dd015a23f55217326820e81d7d9`  
		Last Modified: Fri, 06 Sep 2024 22:26:59 GMT  
		Size: 3.4 MB (3358817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f021a2a9854b506a06eea76cab86a36ed7f250bd508bceb7666b89053c4796f`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 296.2 KB (296243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafd9592e7a1fd1d027f54305c4e4fb5e20405b9c43009723ba04fca50d77a64`  
		Last Modified: Sat, 07 Sep 2024 11:29:35 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26273b826329a3b2a2131075a0730124bbcac966e967ca93997059bdabaa54e5`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e03ddbd617155d43db86de6cc6f17509498ad050bb00d7ed332bfb33d5e696`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:602e33f9e9fb3c76e4f743791ce778aeff73e573dc2e0ec01a337bb203a457b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 KB (190753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b822904f2f33756cbb47dbffb908b14f75a5e531ca2490395254fdfa860e226`

```dockerfile
```

-	Layers:
	-	`sha256:33f6a549437f27db6e750cfaaa06010f51b58580035b760b72ea1fb72a3da969`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 176.9 KB (176875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb8aed2a37a0588e84955cca589c4f048554636ad5f4869045c82c006d218b9d`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 13.9 KB (13878 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; s390x

```console
$ docker pull registry@sha256:b425d1e159bf0a98fa38fc40e56c65852df7d0f9240eb5e053e707513fb779ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8715c811817919d11e77f2ddb041515209d8660d7c4ba174b9fdea04a8d290`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:915212fdde86cc10e2c0038779562c7f4c2d80f238c5807ab3e6bf15c3f207ae in / 
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
	-	`sha256:e1969bec132c5668fa6607cfae829c75ec87bce5e800a6cb6454687412d3c2db`  
		Last Modified: Fri, 06 Sep 2024 22:49:09 GMT  
		Size: 3.2 MB (3230415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d61c62fb5b980e996ccef94ff2a9d02a5d8bf74ea9f207154f19e6ec47e074b`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 293.9 KB (293885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd490e06e2ae62a247359af493fe767b91aa091c5d8702b061c25d6446091713`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2056d8d717fe1c97e0ea3cadc789fe84ef61ccfceb4ed07c0bd118056015a78d`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48e631184dc020d330d4c0357a3b2b24dbb0715f7dba3c45ce008c90f4d8929`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:85772e4077bc98a05e7e47b5757faf18327329b216ba4be88a132688cfd0895d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 KB (190679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e21b280ca98e362100cecc1fa546a73b58be6a7401768b7cfceeb2f88741404`

```dockerfile
```

-	Layers:
	-	`sha256:1ffeb8bc912295bb8701cab8f24ba9f0434968cc429c8d99c9be67b8f681c4d3`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 176.8 KB (176841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b451a8f2dbf54a608c1656d3645a71e4cb398a740a2401fbdfec874074f4fa8f`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 13.8 KB (13838 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8.3`

```console
$ docker pull registry@sha256:2138d01b38545123ac695fd532c666c7ee0a37781358c15737297770586d11a9
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
$ docker pull registry@sha256:5e8c7f954d64eb89a98a3f84b6dd1e1f4a9cf3d25e41575dd0a96d3e3363cba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10114050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ef5b734af47dc41ff2fb442f287ee08c7da31dddb3759616a8f693f0f346a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
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
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ab09421e5ab31796387697888ea35062381139bc482bd424a44d8641207945`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 293.4 KB (293370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40960af72c1c69115fac00e5200d74c78f60acdaf51c7218166781e86b4ea9c1`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bb1dbb377ee0338b3b86dae5d6a2e5530fe03d188d552578f425be24bdf64a`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a538cc9b1ae3c5b339a8c01b77a23b3d6d28a634d05c9ec27f753389931e0552`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:7dfb23ec91fbf29941cf3d5a8be16e7555166b982b3e6544e0662811cd4d15d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 KB (192633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076f378091a9c20d30c1ac87002851f45f1b9f388dd8e769a17a80f5a49f0355`

```dockerfile
```

-	Layers:
	-	`sha256:a6009a951c3d76c9132bc57451567238636504b66bcae0b08de8f56de249cd88`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 178.8 KB (178795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccc12179a4b433c440436a1c0c56fd5b78d8430128385c97d9f112a25f184f81`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
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
$ docker pull registry@sha256:17f2b46e3f28d86aa0d051552cecaf9e09f7d0f664a80ef4745d1102f7ff2323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9cf76bb104e1d7bf59b23d4b9af832bf75736893c2fece60665bfdc73006bcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:c2dbff469fced00345f9627d1efd892f94d53dbb31a6485fa9411b2fb1b4840f in / 
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
	-	`sha256:720f3032cd1105e6311c8adee3ee0f3b6827bec2c48f1cfff486a347ad22f05c`  
		Last Modified: Fri, 06 Sep 2024 22:44:58 GMT  
		Size: 3.3 MB (3340347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d259642272e58761a700b543b776612d3c845e0c6b44ed1e0310391decbecafb`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 295.8 KB (295824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e496f3330122160bc7189304622bf8abe6a2ae218ccb0e821b2021893d48b68`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 5.8 MB (5824732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e961822193ae9a01b0dedeb124ed4268485dfaad16b6e3a3de2315601dafeeaa`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98a2db964ee0b7107b82305b8911d3f3395e05039b068f8aebff82fd57adb0e`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:149c40af501a6e96b60df39771ace01be069225a9a68758f16e22b4983839a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 KB (192989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526f372eda7cba4b0edfcd064c841e4bb19756e86a819eb949673810c7a72610`

```dockerfile
```

-	Layers:
	-	`sha256:67572e10d475c7d60d02a046567b7a8e5e5993e309fb3272515c9b042bbf4582`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 178.9 KB (178851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4124005187b1cab3478c87c0d84a7a2431ba0f1f0800238426711c35204460ed`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 14.1 KB (14138 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; ppc64le

```console
$ docker pull registry@sha256:1a5dd6584bd8161465f83b444c25bfda8da69e06fbe041fade4f1b32b3c776df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c749e4a884836945250c96e95c49968f6fa318e502278f2381e98a531c67a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:2b1a723fec64c757d924d7e1e007f92ef7f3d7e7c91198b52ccf7c47d5a4d10a in / 
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
	-	`sha256:09f69d5d2e4b62e458d29b2e4d2542a265853dd015a23f55217326820e81d7d9`  
		Last Modified: Fri, 06 Sep 2024 22:26:59 GMT  
		Size: 3.4 MB (3358817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f021a2a9854b506a06eea76cab86a36ed7f250bd508bceb7666b89053c4796f`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 296.2 KB (296243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafd9592e7a1fd1d027f54305c4e4fb5e20405b9c43009723ba04fca50d77a64`  
		Last Modified: Sat, 07 Sep 2024 11:29:35 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26273b826329a3b2a2131075a0730124bbcac966e967ca93997059bdabaa54e5`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e03ddbd617155d43db86de6cc6f17509498ad050bb00d7ed332bfb33d5e696`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:602e33f9e9fb3c76e4f743791ce778aeff73e573dc2e0ec01a337bb203a457b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 KB (190753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b822904f2f33756cbb47dbffb908b14f75a5e531ca2490395254fdfa860e226`

```dockerfile
```

-	Layers:
	-	`sha256:33f6a549437f27db6e750cfaaa06010f51b58580035b760b72ea1fb72a3da969`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 176.9 KB (176875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb8aed2a37a0588e84955cca589c4f048554636ad5f4869045c82c006d218b9d`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 13.9 KB (13878 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; s390x

```console
$ docker pull registry@sha256:b425d1e159bf0a98fa38fc40e56c65852df7d0f9240eb5e053e707513fb779ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8715c811817919d11e77f2ddb041515209d8660d7c4ba174b9fdea04a8d290`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:915212fdde86cc10e2c0038779562c7f4c2d80f238c5807ab3e6bf15c3f207ae in / 
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
	-	`sha256:e1969bec132c5668fa6607cfae829c75ec87bce5e800a6cb6454687412d3c2db`  
		Last Modified: Fri, 06 Sep 2024 22:49:09 GMT  
		Size: 3.2 MB (3230415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d61c62fb5b980e996ccef94ff2a9d02a5d8bf74ea9f207154f19e6ec47e074b`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 293.9 KB (293885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd490e06e2ae62a247359af493fe767b91aa091c5d8702b061c25d6446091713`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2056d8d717fe1c97e0ea3cadc789fe84ef61ccfceb4ed07c0bd118056015a78d`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48e631184dc020d330d4c0357a3b2b24dbb0715f7dba3c45ce008c90f4d8929`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:85772e4077bc98a05e7e47b5757faf18327329b216ba4be88a132688cfd0895d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 KB (190679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e21b280ca98e362100cecc1fa546a73b58be6a7401768b7cfceeb2f88741404`

```dockerfile
```

-	Layers:
	-	`sha256:1ffeb8bc912295bb8701cab8f24ba9f0434968cc429c8d99c9be67b8f681c4d3`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 176.8 KB (176841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b451a8f2dbf54a608c1656d3645a71e4cb398a740a2401fbdfec874074f4fa8f`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 13.8 KB (13838 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:3.0.0-beta.1`

```console
$ docker pull registry@sha256:3f87f022afbbd8e1d7cc0e05dbaf3a4f5a5c542a32a016f09f41b2842796b654
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
$ docker pull registry@sha256:4dadcb49d5b624621b91e4e1601443c4bb1cc8c12a60814615b50553c4427900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb1aa51f14ee4feb9d22b7348284bfafe8134d005f766acc175abb952023f65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 10 Jul 2024 13:39:47 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde81e3b1f2e936b2e308a575d4d2d9810b2548cff9033838f4dca05d97855c3`  
		Last Modified: Fri, 06 Sep 2024 23:22:32 GMT  
		Size: 290.9 KB (290876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97dc90ef85c0c60bfd5b77fa9767c6a1e00d7348a8b34c359e897af814d89a7`  
		Last Modified: Fri, 06 Sep 2024 23:22:32 GMT  
		Size: 11.0 MB (10995741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ed82f9d934821eca7e7a10ad28050adb4d0bb09403d72db2fe256dfd2b9330`  
		Last Modified: Fri, 06 Sep 2024 23:22:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8c17bf4f26b7868b410781be53dbec7b15803096f237fb197f8630b3a4e9c8`  
		Last Modified: Fri, 06 Sep 2024 23:22:32 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-beta.1` - unknown; unknown

```console
$ docker pull registry@sha256:c7608113145b52a523e434507e78032daaa59bf12dcac566f2b202d18ceaaf70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 KB (256101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b68481b9c631513db047fedf1e22e581f933b7df655eded3b07687ddc5f4bf`

```dockerfile
```

-	Layers:
	-	`sha256:9e853e662071495d603f05ffc2e9371db81ab55e7353f0fe77ed163a2798b592`  
		Last Modified: Fri, 06 Sep 2024 23:22:32 GMT  
		Size: 243.1 KB (243147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be3b1e8f7a29e2850b1b827f023025232785b50ce7b693d67e2935c0ab9fd98`  
		Last Modified: Fri, 06 Sep 2024 23:22:32 GMT  
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
$ docker pull registry@sha256:9e3e5247419302ca49c999c7f773b0cc9b4366003eabbac74c0edf4683f7f22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14547234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc461b3ced4f342674bd26c421f0220ab03bb248d7ee506fd3479dd4f985db2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 10 Jul 2024 13:39:47 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cac1a4b065c9c855fffe18402bb1a7f6f7e3d3c997a5d6efece488ea46d240e`  
		Last Modified: Sat, 07 Sep 2024 05:15:25 GMT  
		Size: 293.5 KB (293502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0bc398a1d9478da3f04b59dd9c49a845b3c3936a869e45e407ad444d3577a7`  
		Last Modified: Sat, 07 Sep 2024 11:35:04 GMT  
		Size: 10.2 MB (10165474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9182063b4d248c515193c02f04637b187166b16d591a0b05b0a9943386a2ec1`  
		Last Modified: Sat, 07 Sep 2024 11:35:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf14af679670848595909fe63b0cc77760a3f8f209ef32a573949a94ca61f5dc`  
		Last Modified: Sat, 07 Sep 2024 11:35:03 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-beta.1` - unknown; unknown

```console
$ docker pull registry@sha256:adc626cd710c07d3f07d77ef517c363c82bf35309989b3418116a139e12feb49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 KB (256385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c722b62f209b6fb7c5d5e93bac8e9f9f6650c94960c1785ab812d7a1adbbc7a2`

```dockerfile
```

-	Layers:
	-	`sha256:c9678777ba4168e16f6a33c94ad82eaa147c88b2f6c379da1c3e7f0ba5ade853`  
		Last Modified: Sat, 07 Sep 2024 11:35:03 GMT  
		Size: 243.2 KB (243167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7596bb10e305abb8ce6e72c84de138111abdee498bb946d83d4719c66333a515`  
		Last Modified: Sat, 07 Sep 2024 11:35:03 GMT  
		Size: 13.2 KB (13218 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-beta.1` - linux; ppc64le

```console
$ docker pull registry@sha256:e3b04e797bec8ad03ed67a775c3a24e97f96042f114ea64b2e7f407585679f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13787879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1d7f86d11d9d5e7c7a0c07b6e3b520a0668de55d0401798c54558e97ce5fbc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 10 Jul 2024 13:39:47 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f84e45b04d7b25e1e5813237e957c825c0ed033a4dca7930a9882de8427e0e`  
		Last Modified: Sat, 07 Sep 2024 06:52:19 GMT  
		Size: 294.0 KB (294009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03456d0b340e3a9efccd71ccbf8b88ba0c7642ef6af664690ccd25bb8a5c66ea`  
		Last Modified: Sat, 07 Sep 2024 11:29:05 GMT  
		Size: 9.9 MB (9920841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceb7f4319af753aa60cd9393c8ad3e18c4b008e5362e288f50c3b4670010919`  
		Last Modified: Sat, 07 Sep 2024 11:29:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae85350431ec59c80842f94b1d85867b714bebde545705e47ce2ef9814e8202b`  
		Last Modified: Sat, 07 Sep 2024 11:29:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-beta.1` - unknown; unknown

```console
$ docker pull registry@sha256:d270de967dd6c5c4c7490ea76c4ec3a1301337d6b1624322ae887243f1fb83a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 KB (254181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef136101fc96c4ad091b059553c6f1f36e760048cd9653a8618be0a5ffdbd2d`

```dockerfile
```

-	Layers:
	-	`sha256:648cc30eaa7bc13f0bc5466235b6a9f0c5127737c9234475986bd099409da88b`  
		Last Modified: Sat, 07 Sep 2024 11:29:04 GMT  
		Size: 241.2 KB (241209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4088851c4b72aaec543a328d220c9f9213dbd1ba08531069612f3089ffeeb514`  
		Last Modified: Sat, 07 Sep 2024 11:29:04 GMT  
		Size: 13.0 KB (12972 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-beta.1` - linux; s390x

```console
$ docker pull registry@sha256:4461f8c5ed534273c2439d732095cea3d899eef7e5a8681945c20879c1a60846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14299512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8dfad1241c07b25c9757872cb0b90e71c0f09234eba74f6a037790493b43fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 10 Jul 2024 13:39:47 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17125b2ca65c3fc030a73292bd9a81e96c5921e35f14f3aa5165a3777ebe8b5`  
		Last Modified: Sat, 07 Sep 2024 02:36:48 GMT  
		Size: 291.9 KB (291892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d971fad0e3da92233c84c6862c31910a0523de78b77d6bbb3e7b1e2ae7562f3`  
		Last Modified: Sat, 07 Sep 2024 10:34:04 GMT  
		Size: 10.5 MB (10545413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038c06e28b22c2aa66faeec973a780ffdac2b2c9018ff6de4942fe99aec941af`  
		Last Modified: Sat, 07 Sep 2024 10:34:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b364e67255b7cae78c55e6d70d8cd4cdcae3213cdce35a6e3a074df17b4adb`  
		Last Modified: Sat, 07 Sep 2024 10:34:04 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-beta.1` - unknown; unknown

```console
$ docker pull registry@sha256:cc9a9f182eac9def5ca54b26fb87065a6c89e6ac744b45a671d23bea1c34432f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 KB (254133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3918eb55011883b698eb54f595a97f04b7c81bd0d9ac156b3db1342ab1079bb1`

```dockerfile
```

-	Layers:
	-	`sha256:84617eea3de0b71e42a73d90ae919f3dbb8ec2bdcf00faa11c11f1073166ff5f`  
		Last Modified: Sat, 07 Sep 2024 10:34:04 GMT  
		Size: 241.2 KB (241179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4defdb53c617065ef09c54de2728a9de7b634221aec7b0bdd86a69b85f59c20e`  
		Last Modified: Sat, 07 Sep 2024 10:34:04 GMT  
		Size: 13.0 KB (12954 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:latest`

```console
$ docker pull registry@sha256:2138d01b38545123ac695fd532c666c7ee0a37781358c15737297770586d11a9
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
$ docker pull registry@sha256:5e8c7f954d64eb89a98a3f84b6dd1e1f4a9cf3d25e41575dd0a96d3e3363cba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10114050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ef5b734af47dc41ff2fb442f287ee08c7da31dddb3759616a8f693f0f346a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
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
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ab09421e5ab31796387697888ea35062381139bc482bd424a44d8641207945`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 293.4 KB (293370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40960af72c1c69115fac00e5200d74c78f60acdaf51c7218166781e86b4ea9c1`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bb1dbb377ee0338b3b86dae5d6a2e5530fe03d188d552578f425be24bdf64a`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a538cc9b1ae3c5b339a8c01b77a23b3d6d28a634d05c9ec27f753389931e0552`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:7dfb23ec91fbf29941cf3d5a8be16e7555166b982b3e6544e0662811cd4d15d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 KB (192633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076f378091a9c20d30c1ac87002851f45f1b9f388dd8e769a17a80f5a49f0355`

```dockerfile
```

-	Layers:
	-	`sha256:a6009a951c3d76c9132bc57451567238636504b66bcae0b08de8f56de249cd88`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
		Size: 178.8 KB (178795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccc12179a4b433c440436a1c0c56fd5b78d8430128385c97d9f112a25f184f81`  
		Last Modified: Fri, 06 Sep 2024 23:22:41 GMT  
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
$ docker pull registry@sha256:17f2b46e3f28d86aa0d051552cecaf9e09f7d0f664a80ef4745d1102f7ff2323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9cf76bb104e1d7bf59b23d4b9af832bf75736893c2fece60665bfdc73006bcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:c2dbff469fced00345f9627d1efd892f94d53dbb31a6485fa9411b2fb1b4840f in / 
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
	-	`sha256:720f3032cd1105e6311c8adee3ee0f3b6827bec2c48f1cfff486a347ad22f05c`  
		Last Modified: Fri, 06 Sep 2024 22:44:58 GMT  
		Size: 3.3 MB (3340347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d259642272e58761a700b543b776612d3c845e0c6b44ed1e0310391decbecafb`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 295.8 KB (295824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e496f3330122160bc7189304622bf8abe6a2ae218ccb0e821b2021893d48b68`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 5.8 MB (5824732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e961822193ae9a01b0dedeb124ed4268485dfaad16b6e3a3de2315601dafeeaa`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98a2db964ee0b7107b82305b8911d3f3395e05039b068f8aebff82fd57adb0e`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:149c40af501a6e96b60df39771ace01be069225a9a68758f16e22b4983839a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 KB (192989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526f372eda7cba4b0edfcd064c841e4bb19756e86a819eb949673810c7a72610`

```dockerfile
```

-	Layers:
	-	`sha256:67572e10d475c7d60d02a046567b7a8e5e5993e309fb3272515c9b042bbf4582`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 178.9 KB (178851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4124005187b1cab3478c87c0d84a7a2431ba0f1f0800238426711c35204460ed`  
		Last Modified: Sat, 07 Sep 2024 11:35:24 GMT  
		Size: 14.1 KB (14138 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:1a5dd6584bd8161465f83b444c25bfda8da69e06fbe041fade4f1b32b3c776df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c749e4a884836945250c96e95c49968f6fa318e502278f2381e98a531c67a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:2b1a723fec64c757d924d7e1e007f92ef7f3d7e7c91198b52ccf7c47d5a4d10a in / 
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
	-	`sha256:09f69d5d2e4b62e458d29b2e4d2542a265853dd015a23f55217326820e81d7d9`  
		Last Modified: Fri, 06 Sep 2024 22:26:59 GMT  
		Size: 3.4 MB (3358817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f021a2a9854b506a06eea76cab86a36ed7f250bd508bceb7666b89053c4796f`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 296.2 KB (296243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafd9592e7a1fd1d027f54305c4e4fb5e20405b9c43009723ba04fca50d77a64`  
		Last Modified: Sat, 07 Sep 2024 11:29:35 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26273b826329a3b2a2131075a0730124bbcac966e967ca93997059bdabaa54e5`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e03ddbd617155d43db86de6cc6f17509498ad050bb00d7ed332bfb33d5e696`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:602e33f9e9fb3c76e4f743791ce778aeff73e573dc2e0ec01a337bb203a457b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 KB (190753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b822904f2f33756cbb47dbffb908b14f75a5e531ca2490395254fdfa860e226`

```dockerfile
```

-	Layers:
	-	`sha256:33f6a549437f27db6e750cfaaa06010f51b58580035b760b72ea1fb72a3da969`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 176.9 KB (176875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb8aed2a37a0588e84955cca589c4f048554636ad5f4869045c82c006d218b9d`  
		Last Modified: Sat, 07 Sep 2024 11:29:34 GMT  
		Size: 13.9 KB (13878 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:b425d1e159bf0a98fa38fc40e56c65852df7d0f9240eb5e053e707513fb779ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8715c811817919d11e77f2ddb041515209d8660d7c4ba174b9fdea04a8d290`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:915212fdde86cc10e2c0038779562c7f4c2d80f238c5807ab3e6bf15c3f207ae in / 
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
	-	`sha256:e1969bec132c5668fa6607cfae829c75ec87bce5e800a6cb6454687412d3c2db`  
		Last Modified: Fri, 06 Sep 2024 22:49:09 GMT  
		Size: 3.2 MB (3230415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d61c62fb5b980e996ccef94ff2a9d02a5d8bf74ea9f207154f19e6ec47e074b`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 293.9 KB (293885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd490e06e2ae62a247359af493fe767b91aa091c5d8702b061c25d6446091713`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2056d8d717fe1c97e0ea3cadc789fe84ef61ccfceb4ed07c0bd118056015a78d`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48e631184dc020d330d4c0357a3b2b24dbb0715f7dba3c45ce008c90f4d8929`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:85772e4077bc98a05e7e47b5757faf18327329b216ba4be88a132688cfd0895d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 KB (190679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e21b280ca98e362100cecc1fa546a73b58be6a7401768b7cfceeb2f88741404`

```dockerfile
```

-	Layers:
	-	`sha256:1ffeb8bc912295bb8701cab8f24ba9f0434968cc429c8d99c9be67b8f681c4d3`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 176.8 KB (176841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b451a8f2dbf54a608c1656d3645a71e4cb398a740a2401fbdfec874074f4fa8f`  
		Last Modified: Sat, 07 Sep 2024 10:34:32 GMT  
		Size: 13.8 KB (13838 bytes)  
		MIME: application/vnd.in-toto+json
