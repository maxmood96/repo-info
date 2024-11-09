<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.3`](#registry283)
-	[`registry:3.0.0-rc.1`](#registry300-rc1)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:ac0192b549007e22998eb74e8d8488dcfe70f1489520c3b144a6047ac5efbe90
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
$ docker pull registry@sha256:901d40a108aed80d1505bbeb550a071e9bb446e3f1d6450df736605f4d268291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9477619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f15b5e0c5bd8d732d80e973f9637029d722de6d6bcb28f780aab3ee40689bc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:913c69868c0da53176694491758ffca10da8b3ad091f3a77ceecca0aafde5a3a in / 
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
	-	`sha256:16389c65503225c1689cfacdb908862a7eb0642dce6a146f5db303dfbf64a0e9`  
		Last Modified: Fri, 06 Sep 2024 22:50:08 GMT  
		Size: 3.2 MB (3158924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53caa565094144b6fadef5a2447c8653342a554052b9dc9adf3107ca8ea97f94`  
		Last Modified: Sat, 07 Sep 2024 12:19:45 GMT  
		Size: 294.0 KB (294010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33b8a998c8c017e8dcef3b81cb778bdf1333a2951adccc83190861e347d5de1`  
		Last Modified: Sat, 07 Sep 2024 12:19:45 GMT  
		Size: 6.0 MB (6024101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98e02dc5ff421f51ba8981a038f2379641c6c19ca86bdb15cd97e261ea97cfd`  
		Last Modified: Sat, 07 Sep 2024 12:19:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e35c22ecdda67eb46cbedea9fc7ded2f601258ba3064290c7a9f2fe79c5890`  
		Last Modified: Sat, 07 Sep 2024 12:19:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:052c8dbdc75952271a17c2f88fba6ef9a90cafc4c836b5d5b1a5eebeac0e9b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 KB (13702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e27b1534a66495a500559c61ecaaf83340fcaa73ebe30ada126543e37970692`

```dockerfile
```

-	Layers:
	-	`sha256:f92a66b62ddb32746c276e0261bf2f9a18c15c098ac490dadb9b6eacd2aa68a9`  
		Last Modified: Sat, 07 Sep 2024 12:19:44 GMT  
		Size: 13.7 KB (13702 bytes)  
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
$ docker pull registry@sha256:ac0192b549007e22998eb74e8d8488dcfe70f1489520c3b144a6047ac5efbe90
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
$ docker pull registry@sha256:901d40a108aed80d1505bbeb550a071e9bb446e3f1d6450df736605f4d268291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9477619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f15b5e0c5bd8d732d80e973f9637029d722de6d6bcb28f780aab3ee40689bc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:913c69868c0da53176694491758ffca10da8b3ad091f3a77ceecca0aafde5a3a in / 
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
	-	`sha256:16389c65503225c1689cfacdb908862a7eb0642dce6a146f5db303dfbf64a0e9`  
		Last Modified: Fri, 06 Sep 2024 22:50:08 GMT  
		Size: 3.2 MB (3158924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53caa565094144b6fadef5a2447c8653342a554052b9dc9adf3107ca8ea97f94`  
		Last Modified: Sat, 07 Sep 2024 12:19:45 GMT  
		Size: 294.0 KB (294010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33b8a998c8c017e8dcef3b81cb778bdf1333a2951adccc83190861e347d5de1`  
		Last Modified: Sat, 07 Sep 2024 12:19:45 GMT  
		Size: 6.0 MB (6024101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98e02dc5ff421f51ba8981a038f2379641c6c19ca86bdb15cd97e261ea97cfd`  
		Last Modified: Sat, 07 Sep 2024 12:19:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e35c22ecdda67eb46cbedea9fc7ded2f601258ba3064290c7a9f2fe79c5890`  
		Last Modified: Sat, 07 Sep 2024 12:19:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:052c8dbdc75952271a17c2f88fba6ef9a90cafc4c836b5d5b1a5eebeac0e9b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 KB (13702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e27b1534a66495a500559c61ecaaf83340fcaa73ebe30ada126543e37970692`

```dockerfile
```

-	Layers:
	-	`sha256:f92a66b62ddb32746c276e0261bf2f9a18c15c098ac490dadb9b6eacd2aa68a9`  
		Last Modified: Sat, 07 Sep 2024 12:19:44 GMT  
		Size: 13.7 KB (13702 bytes)  
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
$ docker pull registry@sha256:ac0192b549007e22998eb74e8d8488dcfe70f1489520c3b144a6047ac5efbe90
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
$ docker pull registry@sha256:901d40a108aed80d1505bbeb550a071e9bb446e3f1d6450df736605f4d268291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9477619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f15b5e0c5bd8d732d80e973f9637029d722de6d6bcb28f780aab3ee40689bc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:913c69868c0da53176694491758ffca10da8b3ad091f3a77ceecca0aafde5a3a in / 
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
	-	`sha256:16389c65503225c1689cfacdb908862a7eb0642dce6a146f5db303dfbf64a0e9`  
		Last Modified: Fri, 06 Sep 2024 22:50:08 GMT  
		Size: 3.2 MB (3158924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53caa565094144b6fadef5a2447c8653342a554052b9dc9adf3107ca8ea97f94`  
		Last Modified: Sat, 07 Sep 2024 12:19:45 GMT  
		Size: 294.0 KB (294010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33b8a998c8c017e8dcef3b81cb778bdf1333a2951adccc83190861e347d5de1`  
		Last Modified: Sat, 07 Sep 2024 12:19:45 GMT  
		Size: 6.0 MB (6024101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98e02dc5ff421f51ba8981a038f2379641c6c19ca86bdb15cd97e261ea97cfd`  
		Last Modified: Sat, 07 Sep 2024 12:19:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e35c22ecdda67eb46cbedea9fc7ded2f601258ba3064290c7a9f2fe79c5890`  
		Last Modified: Sat, 07 Sep 2024 12:19:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:052c8dbdc75952271a17c2f88fba6ef9a90cafc4c836b5d5b1a5eebeac0e9b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 KB (13702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e27b1534a66495a500559c61ecaaf83340fcaa73ebe30ada126543e37970692`

```dockerfile
```

-	Layers:
	-	`sha256:f92a66b62ddb32746c276e0261bf2f9a18c15c098ac490dadb9b6eacd2aa68a9`  
		Last Modified: Sat, 07 Sep 2024 12:19:44 GMT  
		Size: 13.7 KB (13702 bytes)  
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

## `registry:3.0.0-rc.1`

```console
$ docker pull registry@sha256:c938cc272d093fce3fdae4a317a8661c060f84c6e03639fb8a00e92255071b38
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
$ docker pull registry@sha256:f9e64f882570929c59a2e6f15c52f970b20d325b5dd456d6236c52ee4a064999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18233180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d68aeb8668335a91bd8e374b6afc1af3cd5e0848334ec48c40cbc9c9cabf1d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d123c57e7adc49f9c3d0b6b772746454893f7307e7459354d6424a68bc78a7d1`  
		Last Modified: Fri, 08 Nov 2024 21:58:39 GMT  
		Size: 290.9 KB (290884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587c87b745b4321e40c43ec01e534efbd418fe937859bf353464623bd9e298f0`  
		Last Modified: Fri, 08 Nov 2024 21:58:39 GMT  
		Size: 14.3 MB (14317879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21df87ff4e0e63211927dcd64d3f047d5bdf0dd16bc6082686679d4d0983504f`  
		Last Modified: Fri, 08 Nov 2024 21:58:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059a3e603f1c19b23b96b808ff1b1b4e9634389fcd133a2a48b50281ad205d73`  
		Last Modified: Fri, 08 Nov 2024 21:58:39 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.1` - unknown; unknown

```console
$ docker pull registry@sha256:4d4a7d0f36fbb5450a6a8210664f979961ba64d48239b7b94ae39c6c4fd6d9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 KB (271686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a567f728b9f4be5f158f1905ed8c931e6d8a1c642426bc92e373e2b4c343455`

```dockerfile
```

-	Layers:
	-	`sha256:9ec429f7ce2ed20044e4469d62eddbbc83ff089020ceccc411884ee5f55c0740`  
		Last Modified: Fri, 08 Nov 2024 21:58:39 GMT  
		Size: 258.4 KB (258391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccdcd4ee91fbb4a471566a0ef1058f72db19a33070861b6b6faea5bb515c916c`  
		Last Modified: Fri, 08 Nov 2024 21:58:39 GMT  
		Size: 13.3 KB (13295 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.1` - linux; arm variant v6

```console
$ docker pull registry@sha256:033866d8fd421722cf0f4e6467cc0d016ae3c240c001f4b6b9cb71b50f24c3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17115054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c53cc15dbc776dd811a8f46c7bd1de5702e6128d79e01ba95daae7fde3c087`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b15e82573debca2fd0fd40f07ac032fefe7f9180bd45f4f9cf2c2afde7d486`  
		Last Modified: Sat, 07 Sep 2024 02:30:42 GMT  
		Size: 291.8 KB (291766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1b9f860da494743ac29acc7f9e23dabb7771d07e1986d34b6f5742d972a602`  
		Last Modified: Fri, 08 Nov 2024 21:58:34 GMT  
		Size: 13.5 MB (13456171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ccab531e202d8273751ea51108604d37d3b77e82f3a485f11a76be07c9f5ea`  
		Last Modified: Fri, 08 Nov 2024 21:58:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee4c77c5e993746f64eccbcd6b11ec93c15a6fd5b46c0065d3c5674835baa32`  
		Last Modified: Fri, 08 Nov 2024 21:58:33 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.1` - unknown; unknown

```console
$ docker pull registry@sha256:8f68842586a1a2520ab869876c18158a23083e189141dbf21b6606f5663f84e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f6b1da4988fa2a33a6a02042e90213cd431d0369a54b2327a9a007a9827418`

```dockerfile
```

-	Layers:
	-	`sha256:f5f22e21764d41917eeda7c2c255e54d6bdcec16ec6342ba28bbb23e91d7023d`  
		Last Modified: Fri, 08 Nov 2024 21:58:33 GMT  
		Size: 13.1 KB (13140 bytes)  
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
$ docker pull registry@sha256:659110c7344a6c936ce8e6f5f7552be5c9043c6f9dc0cc448aeb50a81f540df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17603348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5bff817b237138cdcbc62d8562499fafa14ddfad21ef2e288212f82b03c8f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a9dd7d6fc256d156365346b32d280a887ef75129be8a63ce1612b621fc9714`  
		Last Modified: Thu, 07 Nov 2024 03:00:57 GMT  
		Size: 293.5 KB (293527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fce3deac3c0a25b0998752d01ef27ac1f0ef71263dcfd1c48c7b7136354f430`  
		Last Modified: Fri, 08 Nov 2024 21:58:41 GMT  
		Size: 13.2 MB (13221564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2e1375bbc9b29b4005932e3ee9a19433a9a62397e711af0eac5e7b32f0d837`  
		Last Modified: Fri, 08 Nov 2024 21:58:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee4c77c5e993746f64eccbcd6b11ec93c15a6fd5b46c0065d3c5674835baa32`  
		Last Modified: Fri, 08 Nov 2024 21:58:33 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.1` - unknown; unknown

```console
$ docker pull registry@sha256:9d7ba0280d2d76cf038d2984a1019429a0f31fba9d9e5f0ce04d0a3ebcba904b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 KB (271784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40498336f60a92af72ac799d1837716ceef4f99aab71f140ed07129e985976f2`

```dockerfile
```

-	Layers:
	-	`sha256:d87dbe050d56f419050d6528b3df687ca1c1ba9e57bd66cdd5d464f5988cc29e`  
		Last Modified: Fri, 08 Nov 2024 21:58:40 GMT  
		Size: 258.4 KB (258411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e260af9ad051f65fd5d5a9f1d761ff9bf624c803ef5510b77bdd6d1513b4b352`  
		Last Modified: Fri, 08 Nov 2024 21:58:40 GMT  
		Size: 13.4 KB (13373 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.1` - linux; ppc64le

```console
$ docker pull registry@sha256:dc2e15b56e47e77f70bf2ed3ec93b78508d6efe11ca0af2da22668ccea3c435e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16766636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e2f5508c9622605144494ba5e0e7ee2b7824d7f52cf7e83621fc54e80d7fae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977bd9456f1b6f8f4f6980e045da412051b1eade2ac61e6b8469b4da52c93c14`  
		Last Modified: Thu, 07 Nov 2024 03:00:59 GMT  
		Size: 294.0 KB (294035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaafd5cd3ff070c087cb37a383d985823d165a06c399d9c6685135cf88433433`  
		Last Modified: Fri, 08 Nov 2024 21:58:38 GMT  
		Size: 12.9 MB (12899572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c712e6bc43ee3f42d296a99a0f88723af4ca1981f3ec8b48c63d010fe27e91db`  
		Last Modified: Fri, 08 Nov 2024 21:58:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45506c78fd34b70a22fc38fc2562b46d839119c2facacada5634e9823a98654e`  
		Last Modified: Fri, 08 Nov 2024 21:58:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.1` - unknown; unknown

```console
$ docker pull registry@sha256:855e992fd5a423f1a0802ae6a337eb54057345e1dfd04afdf95c509db9337e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 KB (269770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced124e3469477424c477e3b2ac0bc81ab6ffc6a3e6715cd5f498b6d3c2ad16b`

```dockerfile
```

-	Layers:
	-	`sha256:328e7ba405a7c144b60a933641cafc84be429a723183ea89d6a6d59946be8ed0`  
		Last Modified: Fri, 08 Nov 2024 21:58:38 GMT  
		Size: 256.5 KB (256453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8be2b93e091981e16bca2c4fcbf0cae711478334c38053257155d9489c14c1c1`  
		Last Modified: Fri, 08 Nov 2024 21:58:37 GMT  
		Size: 13.3 KB (13317 bytes)  
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
$ docker pull registry@sha256:30105a485d864c7771ac076d94532f03aa1e5adfd05c5d84518310ec733c38d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17544059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d21b3317e01198612d066bfdc05a5e66208c7c1916e26b12f5af2529d11b665`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4e1cbd4051c86d195b2fb96cfc17e7a43cdeb3b02d9c627067475b5a4d1cdd`  
		Last Modified: Thu, 07 Nov 2024 03:05:08 GMT  
		Size: 291.9 KB (291897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f25c95f6765f16cb2ae1db2e09c0f72b4f13fbffb5b9a9ec7d677f209b3f87`  
		Last Modified: Fri, 08 Nov 2024 21:59:56 GMT  
		Size: 13.8 MB (13789956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a1bfd7401847425e4543bac5bc1b080c38ed42c26533a24d5d3e0c881b8ad`  
		Last Modified: Fri, 08 Nov 2024 21:59:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89841bfe41836622495c96ce90df9e1cf1b9a81d0b8aa97a0894244e133d24ef`  
		Last Modified: Fri, 08 Nov 2024 21:59:56 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.1` - unknown; unknown

```console
$ docker pull registry@sha256:a4090621d2c56a192916148815fdd20876d24b06620e644ce57388310b4a85a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.7 KB (269723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9eb6e489ec41aa6ba4022232c72c44afa4341b974eb6c2b381c6d63fb0aefb`

```dockerfile
```

-	Layers:
	-	`sha256:61afaa66c69cc2eca466ff56c2f9136265e37a39e618566b024259f1338591a1`  
		Last Modified: Fri, 08 Nov 2024 21:59:56 GMT  
		Size: 256.4 KB (256427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1a1b13ae0b565eb13683a8df6a62feea06fda25991548e317b58cd551c00b4b`  
		Last Modified: Fri, 08 Nov 2024 21:59:56 GMT  
		Size: 13.3 KB (13296 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:latest`

```console
$ docker pull registry@sha256:ac0192b549007e22998eb74e8d8488dcfe70f1489520c3b144a6047ac5efbe90
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
$ docker pull registry@sha256:901d40a108aed80d1505bbeb550a071e9bb446e3f1d6450df736605f4d268291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9477619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f15b5e0c5bd8d732d80e973f9637029d722de6d6bcb28f780aab3ee40689bc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD file:913c69868c0da53176694491758ffca10da8b3ad091f3a77ceecca0aafde5a3a in / 
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
	-	`sha256:16389c65503225c1689cfacdb908862a7eb0642dce6a146f5db303dfbf64a0e9`  
		Last Modified: Fri, 06 Sep 2024 22:50:08 GMT  
		Size: 3.2 MB (3158924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53caa565094144b6fadef5a2447c8653342a554052b9dc9adf3107ca8ea97f94`  
		Last Modified: Sat, 07 Sep 2024 12:19:45 GMT  
		Size: 294.0 KB (294010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33b8a998c8c017e8dcef3b81cb778bdf1333a2951adccc83190861e347d5de1`  
		Last Modified: Sat, 07 Sep 2024 12:19:45 GMT  
		Size: 6.0 MB (6024101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98e02dc5ff421f51ba8981a038f2379641c6c19ca86bdb15cd97e261ea97cfd`  
		Last Modified: Sat, 07 Sep 2024 12:19:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e35c22ecdda67eb46cbedea9fc7ded2f601258ba3064290c7a9f2fe79c5890`  
		Last Modified: Sat, 07 Sep 2024 12:19:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:052c8dbdc75952271a17c2f88fba6ef9a90cafc4c836b5d5b1a5eebeac0e9b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 KB (13702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e27b1534a66495a500559c61ecaaf83340fcaa73ebe30ada126543e37970692`

```dockerfile
```

-	Layers:
	-	`sha256:f92a66b62ddb32746c276e0261bf2f9a18c15c098ac490dadb9b6eacd2aa68a9`  
		Last Modified: Sat, 07 Sep 2024 12:19:44 GMT  
		Size: 13.7 KB (13702 bytes)  
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
