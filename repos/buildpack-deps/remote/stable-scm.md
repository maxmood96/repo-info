## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:1852e94ab84cbd1b15fe0bc5b770b439d7b462f6553e1c5d643bdc0abe5522d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:stable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:06f191eff803ad2e91e6da35baf08f715c791b05d42c9b0b639d4c18a4008afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136914855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6e3ef7d762499cda27d0ba3c0e6e386e095faa430667ccada53029da4cf183`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:94335992e3d60e078488cff7e63b3a3cd0d4ecb66aceece2034b16fd4c01d9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7966589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9588933ab1cc32be8141a06a74d626e1d5167be3091a19c932e8460e1561fe7c`

```dockerfile
```

-	Layers:
	-	`sha256:bc88903454509e8359e55c3e5214f609103c915da61f6e606cf97197531a6f9c`  
		Last Modified: Tue, 01 Jul 2025 04:19:51 GMT  
		Size: 8.0 MB (7958934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbbd76a94589b2a371b4ab788835cd233b916f3d5d851f2fb9a677e752026c18`  
		Last Modified: Tue, 01 Jul 2025 04:19:52 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4bf0949fe07315995529d92f35fb9fafbd34c190a314d1383af31173bddb7012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130721459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6327b50f52d0bf5fcffa82e23f4204eb2f653baf74d47b571eef2703696d130a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d208698d30e75c289cb2ee99e5f2a75a42e11f8e1b4145f8fb1a881298b833`  
		Last Modified: Tue, 01 Jul 2025 01:14:18 GMT  
		Size: 46.0 MB (46026558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3fc3e72f0d51d8e4d2ef852051b722d30ab0273006822b4317029f0c2f0082`  
		Last Modified: Tue, 01 Jul 2025 06:07:13 GMT  
		Size: 22.7 MB (22696790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a0d5b45d8acba98ba50bdd9aa910689d51522b56b3a703832038000177fd5c`  
		Last Modified: Tue, 01 Jul 2025 09:28:16 GMT  
		Size: 62.0 MB (61998111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:891eb5b1c29d47765d61d4a4c433b10a3e1fbb389c2c664f6f4569c443291643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7968523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282e7505c90ce3c0df912dd4312f941e8899959efc556bd0a9493811a1876ca3`

```dockerfile
```

-	Layers:
	-	`sha256:1c6b04825244d7509f78087b11a2fe405107e0cabc08b81796fbcdd324b95cdd`  
		Last Modified: Tue, 01 Jul 2025 13:20:02 GMT  
		Size: 8.0 MB (7960800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb6f796087060df7c791e270443d7a49814cdf1e730a7472394cd2fe8d9da845`  
		Last Modified: Tue, 01 Jul 2025 13:20:03 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2ff4198bcf865923d022cd6d0841c74edcc17a6f2e63516899f3e0cefef65c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125789771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e330ef581600e7fedf524e08d9c7ae8fd8e7e548a5f9fce582ed29faf05b6aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe8855ed7a68d9f8fe7d302fae88c166a75915bfbd2d109d79128b51764e3ec`  
		Last Modified: Wed, 11 Jun 2025 13:11:47 GMT  
		Size: 59.7 MB (59656919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1f001ed674c422cd3c4531484a047ccbb83c77b6b67638904e542b76983d7c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7966586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6685c1ffb1281b5d283499a9d6757caf4d2a965be858d63cc0aaf7720bf4d648`

```dockerfile
```

-	Layers:
	-	`sha256:79994d1fc362a7b02c51ee81563ba29f2e5c5eb7d73ba6731435c516083f534a`  
		Last Modified: Wed, 11 Jun 2025 16:19:54 GMT  
		Size: 8.0 MB (7958863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:107672138441adad9f55e241db0203c1314e708d637f79e53fa33d31e5383bb9`  
		Last Modified: Wed, 11 Jun 2025 16:19:55 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cbaf1b8bf88156c0fdef725edb33c34a5e1e2b69b0a9dc64f0c3211868670db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136253261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c9e0090d3ef403a9382192f9e68672dd37cceebfe69f07a1a19bd30f51ccff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:65450536dc5c794754729d5b04512a9bc4fb57dcf85417dbc5dacc60dd9627f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7971730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a5bf1c52c36a633cc0685e43086a5bfc3f395a73b52eea730922a54c72e41d`

```dockerfile
```

-	Layers:
	-	`sha256:1f5d8b2f028541ffb1bc0ae84dd21954fe2c57c244fe922c2a668e3232e86dd4`  
		Last Modified: Wed, 11 Jun 2025 13:20:01 GMT  
		Size: 8.0 MB (7963983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01e71f401688719f25ef4fe439e2ae61e13ac5f1516109454d94de7cdcbbb3a`  
		Last Modified: Wed, 11 Jun 2025 13:20:01 GMT  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7440bffa3edfe318d5b5272ae65e72c9e0409c758eece13e667eaac1b9d8d0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140559671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4486d446a9af6b6b4fb571faaca94c06d6decc7f6444c49c009e0b05145f52`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952009550cca50c5a8b42bdeb6e9116dacc2baceb5799f97bf16934eed752ae`  
		Last Modified: Tue, 01 Jul 2025 03:20:00 GMT  
		Size: 66.2 MB (66225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:83e054b03e5a5d9ff20dd3290749a077812d71baa3f314f2bfdcd83ae6182fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7962721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3981fba1870d9fd3220ffcf022fb36b7c1e6e56f6c5d97217d29eb2b24b4af10`

```dockerfile
```

-	Layers:
	-	`sha256:cde02496da231e6ac29718044c3cfa791e4dd425cdeeb814faf539c40a9c12c5`  
		Last Modified: Tue, 01 Jul 2025 04:20:11 GMT  
		Size: 8.0 MB (7955093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93e57414e82f867152f2876c6d4a1a8f41be7b69b31077265d5af4e5580f8210`  
		Last Modified: Tue, 01 Jul 2025 04:20:12 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c5fa8aa15c9d9b6d8a8231fdc3bd876bb4cd3ae156165aa0012717d09d5d8b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135682904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beedefecdfca808792d43e8ed0999fa21f700419443b0e4207a8c23b12433573`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:348f1ed415b5b1e1f9982a78ffeb15637cbc5b41f93b83724c5938c2c226a58a`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 48.8 MB (48775597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ad14aceadbd8dec6fff454480e4e098f48c504f528663aa483f102aed68047`  
		Last Modified: Wed, 11 Jun 2025 13:00:39 GMT  
		Size: 23.6 MB (23598558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1117c8734bd4897d340d37aa929ac7b2c46b5a9f691f51a958aabc871f6639b1`  
		Last Modified: Wed, 11 Jun 2025 21:03:24 GMT  
		Size: 63.3 MB (63308749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6206653cbd2aef53c06e2d9a0e2a3c484f1a46ec5abdfd9eae047797fc380aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70985218f874530b5d6fb2a079b9c1603e2f0228173b95fc9ddc7c3f0406ed13`

```dockerfile
```

-	Layers:
	-	`sha256:c8859a87661d317ba7efcac029bcd846de7f4ed57b5780bd3d2bf6626194da60`  
		Last Modified: Wed, 11 Jun 2025 22:20:04 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2b7a6a8365eae7cb84eaef545e9e535253b4e18d59dab48cbe7abb836a2b6dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147840924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a72684b98e0ce1c9adda8eb4061532a51c1a48b86864c1811058d048bf70eab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7082fff0db11ec79e9a3c8fc9c05691e086d30ca51023010805fccbeac2b8dad`  
		Last Modified: Tue, 01 Jul 2025 05:07:55 GMT  
		Size: 25.7 MB (25663667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e6cd79d875ce6ba17d2080d5bd4d0d55f7eec0f6bb923ae0b53e5bec14ef9b`  
		Last Modified: Tue, 01 Jul 2025 10:09:38 GMT  
		Size: 69.8 MB (69840014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:85d7351b117bf2eead92efa7bc23b24eaa6c30eb148d6d1ddf4b344c3f870e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54417a3b3858eb20d4be3b405a46b0d18285faffb284b5267b25b7f336c6460`

```dockerfile
```

-	Layers:
	-	`sha256:0214569cf36d3bf6390b9ceccd417f6e15a1dacbdcba6e0c916afe17bf17e5bd`  
		Last Modified: Tue, 01 Jul 2025 13:20:24 GMT  
		Size: 8.0 MB (7966801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1db99413cbcc3de0205cb045334a53959607d21ffca60d5835ce35c96fa269c6`  
		Last Modified: Tue, 01 Jul 2025 13:20:25 GMT  
		Size: 7.7 KB (7693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6ec2c0b1fcfd242d8e47ea14056ef51248dac763925c891fec157b6864cfb8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134667792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ef3c9e8faf1aafc458b4a19ccb1cc5b5a76a1cca5b6f726c5bdde6ef24d96c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dca9cef3741351ad228dc4986e66f3e324bfb88d5cc9e2b190dd3a3abf7dcf`  
		Last Modified: Tue, 01 Jul 2025 05:30:26 GMT  
		Size: 24.0 MB (24020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff1e32b479a11528098c70ba4af6292099abafcb29e0823d2861c86032c9b0b`  
		Last Modified: Tue, 01 Jul 2025 08:55:44 GMT  
		Size: 63.5 MB (63497964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:633076af373671ac439e1661db1e5c0724f79cf2ff53a16cac4d0578be4891ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7962902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749bdee2495b60249c0a479d3d6cb891e80a844877b0b1c011ed7372ba55727e`

```dockerfile
```

-	Layers:
	-	`sha256:54b1f686b06595c3970c3df3d3f22033614b9e6555fa0097cdf719dfb9594084`  
		Last Modified: Tue, 01 Jul 2025 10:20:15 GMT  
		Size: 8.0 MB (7955247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c708440b09ec17bcfe1583bab83fac03c69d16c70093be8d6223734fc537a46`  
		Last Modified: Tue, 01 Jul 2025 10:20:15 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json
