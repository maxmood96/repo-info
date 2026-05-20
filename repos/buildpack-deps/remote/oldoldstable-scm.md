## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:b4c96554f00dfd1b04fd54d9f50e7cedead81476f7bbb27d774098de99db6e77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c57d426e45fe981d5329d691416132653948e07014e2ef4612719621c5bb7e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124302972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30ee249d13c0c97225996571a9c2ff40ffe33e6160cf3889f8a7201fffe4d3d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:23:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a725631376ff1c8c144d62e01c2dd134ff006899cd43c1aff2afbb3141faf91b`  
		Last Modified: Tue, 19 May 2026 23:23:13 GMT  
		Size: 15.8 MB (15790858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5942943df443b1bc1e709676d52a57b0a7ddee0c58a1602ecf5e2e8b271916d`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 54.7 MB (54743262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8b02d343c0a660fc48cfc3a65b4a0f67f73b29b21c1d8d547e6b27596e74200d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7928693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef342b44eec17a9a6e168c0b24de98036489e0808030a10f6915c8d7a5d2dbb7`

```dockerfile
```

-	Layers:
	-	`sha256:52af8f71d6a41fa75782580a91d8d8bf71a9208e3d418e7256004a63fb552a6d`  
		Last Modified: Wed, 20 May 2026 00:26:18 GMT  
		Size: 7.9 MB (7921377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99a2453f00e82c92de0a2bd031f5e45b88495b46238be7589f84442213c26d78`  
		Last Modified: Wed, 20 May 2026 00:26:17 GMT  
		Size: 7.3 KB (7316 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7a43c229c5ed1a3727982a3ef6a951b4abe04f4cb01fb1d0fc893a2a88d48d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114624408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d307f4e628a697b68d13027523398c59d6b2f718addcbaa5c5da48efec19dc5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:03:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c303da1bd3f277cef3c251ecb02fe6ceb28404700c2776e5e52078361e0d5a63`  
		Last Modified: Tue, 19 May 2026 22:36:43 GMT  
		Size: 49.1 MB (49059808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6159604253fa0b585197db46cb3703cf956f0b1a4d8cb67a661c9f449e5220b`  
		Last Modified: Wed, 20 May 2026 00:03:11 GMT  
		Size: 14.9 MB (14905378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb581721ec88241b5b5ab6b082d3be5546d7889197d205126a49442b917bbba1`  
		Last Modified: Wed, 20 May 2026 01:34:28 GMT  
		Size: 50.7 MB (50659222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:294eb211e84504a7c88bf6965ba365ed68df05b6b005a8414de45baeb13343df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7930159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b0a9e5e1d1a933cba5587d9e6d3867c95a93ada142c166872c75d0296f8cfd2`

```dockerfile
```

-	Layers:
	-	`sha256:68ac6d4fa5496ca8c36b2d9bb2bdabe3499ed1df514b306dfcca599764363d38`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 7.9 MB (7922779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a686d1b079063770de37f043d919569870fa4797348f93c6c041a2694df82d5`  
		Last Modified: Wed, 20 May 2026 01:34:26 GMT  
		Size: 7.4 KB (7380 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1594c94b0efbbeb12cd4bd1ee4d012b3e8e1fd04d4aa4e4f7e411c70f11d7151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122911320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:292a419ab5119d57d202b20a7be03a0d56b0857607134177f56074cc736de4d2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b862d1986560a28dd19f86c2aee630b1502d7f508a9266ed7d99d6f03a48419`  
		Last Modified: Tue, 19 May 2026 23:26:59 GMT  
		Size: 15.8 MB (15774880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522a0e24f23d039a1a5ae21822bccb045bfdedf83da569dc13fb1992e903bbcb`  
		Last Modified: Wed, 20 May 2026 00:27:11 GMT  
		Size: 54.9 MB (54879862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:69721f5e9dc5c70862233e527320de0bfe4959c6717a5b904f38d6b33209c2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7934507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0b4af238f6974b567a0ffafeaa18324f962e63c3a6597871c58913399e91c3`

```dockerfile
```

-	Layers:
	-	`sha256:edd4a1f294dc080e3dd9967d97fa7cdd8bb7a8ca2ca27439ea32eb339232de96`  
		Last Modified: Wed, 20 May 2026 00:27:10 GMT  
		Size: 7.9 MB (7927111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea23ba29396108ed275ed71d1fcea77c24aa68dfbda7c38fcd2818ae64f9f97b`  
		Last Modified: Wed, 20 May 2026 00:27:09 GMT  
		Size: 7.4 KB (7396 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2190dbcc20ff31e1371afaa9afed869ce7e935a543b24299040d80cefed1677e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127051646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72af6c70c8cd822c261ca56e8523530738d476c77d55a3e952b46e98af13a0c8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:44:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e09eb609a6245c10b9cb43e597a7ec3d9e4224f925e717a38f2fb36787a4e7c0`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 54.7 MB (54709050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638a100a514adffbab3ef3834e4740a809fc60c49ad1b434f56a2d8254524b75`  
		Last Modified: Tue, 19 May 2026 23:25:19 GMT  
		Size: 16.3 MB (16295788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927f642862236d0c357dc4ae576bafd5ea8cfb669f7a55b517fc7627c3283f4b`  
		Last Modified: Wed, 20 May 2026 02:45:13 GMT  
		Size: 56.0 MB (56046808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dfba2952259068a47f7b95d4522760d5e68e2b8c71fe06549f46e814b644ccf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7924240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afd7d04ccef95c5670d8c3fe59d82af5465b9392d7bb816860bbfa8048c3b44`

```dockerfile
```

-	Layers:
	-	`sha256:bc675027db216c2d3666ee979a9ef6baad6dabad0a32d2a2046a75213629fe01`  
		Last Modified: Wed, 20 May 2026 02:45:12 GMT  
		Size: 7.9 MB (7916947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fab60e6f06a6d91858212106b13f6141dcc67a96ad878b289a490f6e6d327f9`  
		Last Modified: Wed, 20 May 2026 02:45:11 GMT  
		Size: 7.3 KB (7293 bytes)  
		MIME: application/vnd.in-toto+json
