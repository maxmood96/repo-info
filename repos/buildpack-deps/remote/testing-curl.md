## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:8202971ba44406402e17e1f3341b1a8697f333407334549e1c7df7c39f2b9149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:05d94854f090545a17dabcb74f62e4451e8fb3712a814c785161606975016f55
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71669962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4929eb0318a63ff2edc82a8493199ec1f541063b01d030ea7487a7ea5a841f6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:18 GMT
ADD file:ec1a9a704ae13b142c48069368561119760ccdf3d65d854c426d0dc9c39e60fb in / 
# Fri, 11 Dec 2020 02:05:18 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 16:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 16:55:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e4991c356405721fc787980835bdbf5c529ae12379346a771feb34407c522bd6`  
		Last Modified: Fri, 11 Dec 2020 02:11:29 GMT  
		Size: 53.1 MB (53113553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31d9601ffb01bb76b4b0f063798a4d1ee0fd755c12d07c76aebee06efabb9ba`  
		Last Modified: Thu, 17 Dec 2020 17:23:45 GMT  
		Size: 7.9 MB (7908261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bba58616c17ab814aac1a7b782186b5ce1114f80b807ec7635a3895fecec549`  
		Last Modified: Thu, 17 Dec 2020 17:23:46 GMT  
		Size: 10.6 MB (10648148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ea8258eb0f46cee6ee6e376af9a9d6abd3fc423d76e9577300acecfd6ad2c1b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69351032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c588dbf53ef7521f0529e62869b4460167c6754d3d352a621ea9ce7065e56b21`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:50:29 GMT
ADD file:d4da31b3c934d9b6c8328e7951f06cec1babe1f9674a7a3ee2e87670575ff01c in / 
# Tue, 12 Jan 2021 00:50:30 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:23:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:23:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f9810833d48e3d19cbfbfb8871ba282d104d5bcfae1b19c0c003f9811dbe7c4c`  
		Last Modified: Tue, 12 Jan 2021 00:58:53 GMT  
		Size: 51.5 MB (51487444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d257fe5697f52f59aa0dbdede36db8adf4c0796905b3388832de43ac1e4ab97d`  
		Last Modified: Tue, 12 Jan 2021 01:41:45 GMT  
		Size: 7.5 MB (7527914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c59bb7c72bcd7ff3df84ab37209a928574816146c37f0808619c4b5a6dde4a1`  
		Last Modified: Tue, 12 Jan 2021 01:41:45 GMT  
		Size: 10.3 MB (10335674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a6eb0fadb0bef5514f4f004575e1216dabe7f7d926cd42dacae124aeb512ccd0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66399716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91263701c62ae3a86f4732fc1a5c5feb04184781eda4728fb624f30c788d752d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Jan 2021 23:59:52 GMT
ADD file:ad9ce4dd05291eba636daae5f0b9de510927734ac26dcca6940d93e88b5c5330 in / 
# Mon, 11 Jan 2021 23:59:54 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:11:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:11:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4ecb0a075e68a9a1a4b7394123b05b2811afa9bc0a23170e2e6c42d5ee19a7ac`  
		Last Modified: Tue, 12 Jan 2021 00:09:56 GMT  
		Size: 49.2 MB (49159573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dea32ec53c55b5a19d9fb093241be9ba6e2fe2fd55963111e57d39b0973f01c`  
		Last Modified: Tue, 12 Jan 2021 01:27:54 GMT  
		Size: 7.3 MB (7265094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4b285ad78deb9119d75d41a2decc62fd9676078225d860eec32d20835fa7fb`  
		Last Modified: Tue, 12 Jan 2021 01:27:54 GMT  
		Size: 10.0 MB (9975049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:43d4736915d4b66b791ef4dff3d31645e20816250f5d18a3488cb6a6d678a701
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70923298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f4fd9f3dd5c3e2442efc4b43b90be7e813074e1ce15a875ce5ae7d95b235ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:49 GMT
ADD file:0700c58361c6ae34d399d7ca2a5a6f509980a496c07d319f7455d86b483e7f25 in / 
# Tue, 12 Jan 2021 00:39:56 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:20:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d1e62204d5e176f9e5ef453b346203f7bda9e22ed810a0a4e2c14548d7cc3afe`  
		Last Modified: Tue, 12 Jan 2021 00:50:17 GMT  
		Size: 52.4 MB (52428437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f37b86a934fe39fb5aebaff30977af7d0075b2eeb06b1b794582ae2566dff1`  
		Last Modified: Tue, 12 Jan 2021 01:36:53 GMT  
		Size: 7.8 MB (7840062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0908ecaa573834d3855dd61a0aabaf6565245ab200624d87774802a93f1b2dea`  
		Last Modified: Tue, 12 Jan 2021 01:36:54 GMT  
		Size: 10.7 MB (10654799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:80c9b6633663c3d3ef40e747f413f889c180ba5659edca59087e34d4f622b9d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73270147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d021787519118d73c4b16a3228d88070ed6bcfe960bea56513d8be76fe3530c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:02:21 GMT
ADD file:b10b66385eba9f330914811c1ea9830c75a7d222442b3076a102c918588f96cc in / 
# Fri, 11 Dec 2020 02:02:22 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:06:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:06:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5cec9c367337182f351780e9e280bde357c303f0ca43358fc7dcbe63a9420fb1`  
		Last Modified: Fri, 11 Dec 2020 02:08:35 GMT  
		Size: 54.2 MB (54157004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfed47518c0a507801e5cbe565f2d9072a66d37097eb93c108be072d452bcc7`  
		Last Modified: Thu, 17 Dec 2020 08:22:55 GMT  
		Size: 8.1 MB (8082025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c73ad66a61af03c90dfc68fd0342e7c31aede5c056cec3bb18195e6c3af97ff`  
		Last Modified: Thu, 17 Dec 2020 08:22:55 GMT  
		Size: 11.0 MB (11031118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ae3960e65ddaa86d1d494e5b47f6ea7a197a80903c9ffbebcf03d002e0bcc8e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70414851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5560db536fa1a7b44a1c4f9c4ac634401272c0293aa958e468793c1aa8e7ca2a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 01:15:12 GMT
ADD file:171276d9060030f06df201450c4356d6449f4c6a905d02db7f2371f7ed26b34d in / 
# Tue, 12 Jan 2021 01:15:13 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:45:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:45:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cdc62d8dca2f8e7c324fa9f4efc40193ada4c98be9ca6b3f1388ad903e4bd5d9`  
		Last Modified: Tue, 12 Jan 2021 01:20:56 GMT  
		Size: 52.3 MB (52264790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b87fc90acd9bd7359cfb81de768ce7f4cdc0821db3ed523142fe855433832`  
		Last Modified: Tue, 12 Jan 2021 01:58:49 GMT  
		Size: 7.5 MB (7492735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6084ef3498948096f602b4aac1a0fb7a2dbaa7d5d751897ddec139d2cebb08f`  
		Last Modified: Tue, 12 Jan 2021 01:58:51 GMT  
		Size: 10.7 MB (10657326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7d5f5342fecc7b6d60985b98aafebd691c84ea4c41015271b98b7e86ac8edd6f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76863888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9963398937d68c0d838351bf9544d7bf1a3bc57d10c33dcd28ec26d708000257`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:31:53 GMT
ADD file:9583240ab6aa83a5f964dedeba18905486e879b1839d8329fc20f91cfccdd8d1 in / 
# Fri, 11 Dec 2020 03:32:06 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 11:15:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 11:17:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:018083dcdb1846644d37fb03ece4c9beb51dcb25f9851d01fc02f63c6fb143cc`  
		Last Modified: Fri, 11 Dec 2020 03:40:16 GMT  
		Size: 57.1 MB (57079148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0f8189a228fc57571454349d96c296688da37380e9b69091c6bee4d5f29315`  
		Last Modified: Thu, 17 Dec 2020 13:31:15 GMT  
		Size: 8.4 MB (8363474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765c21425572bad2d7f45674f0aca68f65a0064c986d32df2a8bfa1a71486b9f`  
		Last Modified: Thu, 17 Dec 2020 13:31:15 GMT  
		Size: 11.4 MB (11421266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:db64377208b56bcdb13e9fbc597e03604218318de076730e27676022c27a82a4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70283366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2142411addc51ea4c906ecc47af9ab1e2e2d418309f3c3c69f57b178973d58`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:41 GMT
ADD file:5007beabc318acc6a33d879e231105324ef7801fb709d3d69813b180e883d64f in / 
# Tue, 12 Jan 2021 00:41:44 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 02:07:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 02:07:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f1b527eede6bdcb4cce85e897c3a92fbf04bb476403758d3b535dbf6e388d192`  
		Last Modified: Tue, 12 Jan 2021 00:45:27 GMT  
		Size: 52.1 MB (52107904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f7f4dc3450e7b31e01a1746ba85df290d5b698d495c8ab448923393956e52c`  
		Last Modified: Tue, 12 Jan 2021 02:16:42 GMT  
		Size: 7.6 MB (7649499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945c37e35656a95430c56e2a6bb0a416252a37130eca65d1f3beee38efee696e`  
		Last Modified: Tue, 12 Jan 2021 02:16:42 GMT  
		Size: 10.5 MB (10525963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
