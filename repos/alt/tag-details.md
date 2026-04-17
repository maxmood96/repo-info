<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `alt`

-	[`alt:latest`](#altlatest)
-	[`alt:p10`](#altp10)
-	[`alt:p11`](#altp11)
-	[`alt:sisyphus`](#altsisyphus)

## `alt:latest`

```console
$ docker pull alt@sha256:4c76520bb4935edf624dde76d5e670d54f40938323b185c4c7270881b71fd8ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `alt:latest` - linux; amd64

```console
$ docker pull alt@sha256:fd4ada6a0ed0271b5220a00fb1318523143851a217296b50430bdeafff443332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46310923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8162060838c3d715ae326362b11f29e7aa8379a8df9c3733e2487b7c5195486`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Apr 2026 23:15:57 GMT
LABEL org.opencontainers.image.authors=Alexey Shabalin <shaba@altlinux.org>,Nadezhda Fedorova <fedor@altlinux.org> org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 16 Apr 2026 23:15:57 GMT
ADD alt-p11-x86_64.tar.xz / # buildkit
# Thu, 16 Apr 2026 23:15:57 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 16 Apr 2026 23:15:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1d32bbdd8a35a46c14f20d1eeb28130256717863a0615e4f860363f69792adf1`  
		Last Modified: Thu, 16 Apr 2026 23:16:08 GMT  
		Size: 46.3 MB (46310732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cd105475af997d9bfc38ae4145db77db51afe031c3f683e545fbfc7d4a042f`  
		Last Modified: Thu, 16 Apr 2026 23:16:07 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:4634f12caa0ba0cd7a4a88c37ba3386aff0848dabdc988b18cf36a5c2aaf3aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95516fb70486087ed573781b7348c663be26e04f825e2149e001320251fcd9d0`

```dockerfile
```

-	Layers:
	-	`sha256:69deb00bd4726e0dfed58725c027e709e5734bd579d9ed730fd5407d9cec02e1`  
		Last Modified: Thu, 16 Apr 2026 23:16:07 GMT  
		Size: 2.6 MB (2632321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6549735c3a6f19c5c14ff6aa405ec984f8f203d9e0366c40af22f07d1287871f`  
		Last Modified: Thu, 16 Apr 2026 23:16:07 GMT  
		Size: 6.4 KB (6393 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:latest` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:4c2137b65d700817c5cbc766197db1044ae28f66c3f20ab3794b505a24a45380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45048909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dca2e5e512d51eb86173abc9f46739fed77817bf05a36c1e836de3f5e5c9a6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Apr 2026 23:15:30 GMT
LABEL org.opencontainers.image.authors=Alexey Shabalin <shaba@altlinux.org>,Nadezhda Fedorova <fedor@altlinux.org> org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 16 Apr 2026 23:15:30 GMT
ADD alt-p11-aarch64.tar.xz / # buildkit
# Thu, 16 Apr 2026 23:15:31 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 16 Apr 2026 23:15:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bd5a5b7f15a7de6eb0a5d5a1cb3828c27ff3e2bef91bc1530eca873418b694f4`  
		Last Modified: Thu, 16 Apr 2026 23:15:42 GMT  
		Size: 45.0 MB (45048717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39deafd97db79a8354ed91c12d94b13ef476213f369c22c56461280b248ea064`  
		Last Modified: Thu, 16 Apr 2026 23:15:41 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:41b5157a77a4fe70d2c769ab53c7983120be49fa1730cbaccf4b3cbfa79cec19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce65c4e9aa706c1ef188b7085da04244cb41ff3d12ad114a54a057af5825c74`

```dockerfile
```

-	Layers:
	-	`sha256:b2f2349f82e4036aaae7e957557c7fd437d3c2b4a3b493ad1d1367f7f5dde70d`  
		Last Modified: Thu, 16 Apr 2026 23:15:41 GMT  
		Size: 2.6 MB (2631750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc24470a77a59a253ce15b7490c3e772b0e4e7e273097355de237a2bc9f6887`  
		Last Modified: Thu, 16 Apr 2026 23:15:41 GMT  
		Size: 6.5 KB (6451 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:latest` - linux; 386

```console
$ docker pull alt@sha256:a88bb13e81ad148f51f65534e54150803466c21fea2b23a8f357ad93aa4a2ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46323241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd7342b1e26d8c8f9e233b5ece61d3be9171aacb55cbc66c630da5cf892c2f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Apr 2026 23:16:17 GMT
LABEL org.opencontainers.image.authors=Alexey Shabalin <shaba@altlinux.org>,Nadezhda Fedorova <fedor@altlinux.org> org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 16 Apr 2026 23:16:17 GMT
ADD alt-p11-i586.tar.xz / # buildkit
# Thu, 16 Apr 2026 23:16:18 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 16 Apr 2026 23:16:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1676411b7009be50b237989080f5f14785db662ce1a94719d173f5a430270a90`  
		Last Modified: Thu, 16 Apr 2026 23:16:29 GMT  
		Size: 46.3 MB (46323048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a50c9f2a602b4e28e9ab62d9ddf1a7a8e620b82325e1fb6ff73b54d79a2fa4`  
		Last Modified: Thu, 16 Apr 2026 23:16:28 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:34b63853563ada98b6ae62c163571b03cadd6ff6c14fcc41a29a0cb939078199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b11c340ed504cf39e3abf25483369880bb82d54e49df4f3d1e1071b0fddbd62`

```dockerfile
```

-	Layers:
	-	`sha256:1c0c274d24b7aabb550fed0a5e45261f34e45616c7a2348f1c031c633efdd2de`  
		Last Modified: Thu, 16 Apr 2026 23:16:28 GMT  
		Size: 2.6 MB (2631042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5dadf4b05b7bbb45826166ec3fb86d3f4ebad9013d8da7a90f7d1f7807008a2`  
		Last Modified: Thu, 16 Apr 2026 23:16:28 GMT  
		Size: 6.4 KB (6366 bytes)  
		MIME: application/vnd.in-toto+json

## `alt:p10`

```console
$ docker pull alt@sha256:5edc92edf6bc866824427f05834ffff3f815974fc1cd9840e0dda2492d11ce30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `alt:p10` - linux; amd64

```console
$ docker pull alt@sha256:c96eaf6544cba738fc88d5fa090242750fe2a2fad3a0deefa8540d1a6aca9097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47538056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7387f2d5f20f88d97c4e0b44d22916cee7434f251fe527c25a78bff7c9ce9f66`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Apr 2026 23:14:57 GMT
LABEL org.opencontainers.image.authors=Alexey Shabalin <shaba@altlinux.org>,Nadezhda Fedorova <fedor@altlinux.org> org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 16 Apr 2026 23:14:57 GMT
ADD alt-p10-x86_64.tar.xz / # buildkit
# Thu, 16 Apr 2026 23:14:58 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 16 Apr 2026 23:14:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:40a0b037889829991233d7bdcfe438ab9c45226328875831a28cb3da5bf549d5`  
		Last Modified: Thu, 16 Apr 2026 23:15:09 GMT  
		Size: 47.5 MB (47537865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12341ecce2945b94112b900c6bc7a244fc54a62de09da40813ca957e379b73bd`  
		Last Modified: Thu, 16 Apr 2026 23:15:08 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:30d7b2964678864424e0329c77f6188eea0feb19c54efb123dc806e14c50859e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2602857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef154434eb9779f3c9b2d932160b1abaaaf81c90f20829fb950cedb2bb2698c`

```dockerfile
```

-	Layers:
	-	`sha256:f344fc4f189a7962600f227632e7eb3e5d866c6f588610198d8143fcd91b7d81`  
		Last Modified: Thu, 16 Apr 2026 23:15:09 GMT  
		Size: 2.6 MB (2596756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc15dc3213beb1430dcab67495c10553a8ecb2a4e5db8cb0529f473acad6e5f`  
		Last Modified: Thu, 16 Apr 2026 23:15:08 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p10` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:9eece37270661f14e73b78b217c48b7cd70ec8cda2779412e47c675fc6781ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46706867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936da062195fd24f974d0c5228125b88289783f73a11cd63a48c43b193fde4bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Apr 2026 23:15:06 GMT
LABEL org.opencontainers.image.authors=Alexey Shabalin <shaba@altlinux.org>,Nadezhda Fedorova <fedor@altlinux.org> org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 16 Apr 2026 23:15:06 GMT
ADD alt-p10-aarch64.tar.xz / # buildkit
# Thu, 16 Apr 2026 23:15:07 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 16 Apr 2026 23:15:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4a01e58b207ab09d20614c5a9228271660f45ca3c2ffcda5493b5e9fda30834f`  
		Last Modified: Thu, 16 Apr 2026 23:15:19 GMT  
		Size: 46.7 MB (46706675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b8f1b15362a64b4c7bac8da4e2e2dd28116b5c56340ef01264643c757c200f`  
		Last Modified: Thu, 16 Apr 2026 23:15:17 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:44771f9ec5281c2603ceafebfe55b45414fd6439be8922f9efd867ad9d0142c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2601544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f8faba90d4c2522165d6cb4df832c19dab3b52722c56dcfffe52008ed9ba800`

```dockerfile
```

-	Layers:
	-	`sha256:af955819af0cbfebe6702f20e46851c70510bcd96f0ab10b4ed6401cbae4f690`  
		Last Modified: Thu, 16 Apr 2026 23:15:17 GMT  
		Size: 2.6 MB (2595397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:876f2af5eb5ff9db2aca222d5cd7e6792fe0f2da07430f0737db44427a746f73`  
		Last Modified: Thu, 16 Apr 2026 23:15:17 GMT  
		Size: 6.1 KB (6147 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p10` - linux; 386

```console
$ docker pull alt@sha256:6e47322beadfed1fc6d5c351e528930cfa14843d29fe91075fa5d8c18ed487e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48303999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6fae7a9da4146ee206e807160e14c5ccb242ee0f5367a2879147c811b78adf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Apr 2026 23:15:19 GMT
LABEL org.opencontainers.image.authors=Alexey Shabalin <shaba@altlinux.org>,Nadezhda Fedorova <fedor@altlinux.org> org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 16 Apr 2026 23:15:19 GMT
ADD alt-p10-i586.tar.xz / # buildkit
# Thu, 16 Apr 2026 23:15:19 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 16 Apr 2026 23:15:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cfb8b6f5f2085c2029b3b69c076a425e156e7320e197b1a43478a52a5e37d3f8`  
		Last Modified: Thu, 16 Apr 2026 23:15:32 GMT  
		Size: 48.3 MB (48303808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7592a428fb9e8ac1aad477561e74530e11b795ef6e0ef6155d5885144ebdfd22`  
		Last Modified: Thu, 16 Apr 2026 23:15:30 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:2c758ed2e8e7bae1aeae442a4c2f4abb730ef5ff1b48f471fe8054e6d2903cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2604683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69528ac86dedccfaee116202137577da259003603dd25035ba8cb87ce2428b8c`

```dockerfile
```

-	Layers:
	-	`sha256:de6ff08c78ea0039704985d11deec430547306ab25f8e256f2dc4a92e14bb159`  
		Last Modified: Thu, 16 Apr 2026 23:15:30 GMT  
		Size: 2.6 MB (2598604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17d16196c5197932e6854b9189c0e3e40095ddbf4824e09039fb8c67605bfb2f`  
		Last Modified: Thu, 16 Apr 2026 23:15:30 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.in-toto+json

## `alt:p11`

```console
$ docker pull alt@sha256:4c76520bb4935edf624dde76d5e670d54f40938323b185c4c7270881b71fd8ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `alt:p11` - linux; amd64

```console
$ docker pull alt@sha256:fd4ada6a0ed0271b5220a00fb1318523143851a217296b50430bdeafff443332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46310923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8162060838c3d715ae326362b11f29e7aa8379a8df9c3733e2487b7c5195486`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Apr 2026 23:15:57 GMT
LABEL org.opencontainers.image.authors=Alexey Shabalin <shaba@altlinux.org>,Nadezhda Fedorova <fedor@altlinux.org> org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 16 Apr 2026 23:15:57 GMT
ADD alt-p11-x86_64.tar.xz / # buildkit
# Thu, 16 Apr 2026 23:15:57 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 16 Apr 2026 23:15:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1d32bbdd8a35a46c14f20d1eeb28130256717863a0615e4f860363f69792adf1`  
		Last Modified: Thu, 16 Apr 2026 23:16:08 GMT  
		Size: 46.3 MB (46310732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cd105475af997d9bfc38ae4145db77db51afe031c3f683e545fbfc7d4a042f`  
		Last Modified: Thu, 16 Apr 2026 23:16:07 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:4634f12caa0ba0cd7a4a88c37ba3386aff0848dabdc988b18cf36a5c2aaf3aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95516fb70486087ed573781b7348c663be26e04f825e2149e001320251fcd9d0`

```dockerfile
```

-	Layers:
	-	`sha256:69deb00bd4726e0dfed58725c027e709e5734bd579d9ed730fd5407d9cec02e1`  
		Last Modified: Thu, 16 Apr 2026 23:16:07 GMT  
		Size: 2.6 MB (2632321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6549735c3a6f19c5c14ff6aa405ec984f8f203d9e0366c40af22f07d1287871f`  
		Last Modified: Thu, 16 Apr 2026 23:16:07 GMT  
		Size: 6.4 KB (6393 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p11` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:4c2137b65d700817c5cbc766197db1044ae28f66c3f20ab3794b505a24a45380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45048909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dca2e5e512d51eb86173abc9f46739fed77817bf05a36c1e836de3f5e5c9a6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Apr 2026 23:15:30 GMT
LABEL org.opencontainers.image.authors=Alexey Shabalin <shaba@altlinux.org>,Nadezhda Fedorova <fedor@altlinux.org> org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 16 Apr 2026 23:15:30 GMT
ADD alt-p11-aarch64.tar.xz / # buildkit
# Thu, 16 Apr 2026 23:15:31 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 16 Apr 2026 23:15:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bd5a5b7f15a7de6eb0a5d5a1cb3828c27ff3e2bef91bc1530eca873418b694f4`  
		Last Modified: Thu, 16 Apr 2026 23:15:42 GMT  
		Size: 45.0 MB (45048717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39deafd97db79a8354ed91c12d94b13ef476213f369c22c56461280b248ea064`  
		Last Modified: Thu, 16 Apr 2026 23:15:41 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:41b5157a77a4fe70d2c769ab53c7983120be49fa1730cbaccf4b3cbfa79cec19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce65c4e9aa706c1ef188b7085da04244cb41ff3d12ad114a54a057af5825c74`

```dockerfile
```

-	Layers:
	-	`sha256:b2f2349f82e4036aaae7e957557c7fd437d3c2b4a3b493ad1d1367f7f5dde70d`  
		Last Modified: Thu, 16 Apr 2026 23:15:41 GMT  
		Size: 2.6 MB (2631750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc24470a77a59a253ce15b7490c3e772b0e4e7e273097355de237a2bc9f6887`  
		Last Modified: Thu, 16 Apr 2026 23:15:41 GMT  
		Size: 6.5 KB (6451 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p11` - linux; 386

```console
$ docker pull alt@sha256:a88bb13e81ad148f51f65534e54150803466c21fea2b23a8f357ad93aa4a2ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46323241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd7342b1e26d8c8f9e233b5ece61d3be9171aacb55cbc66c630da5cf892c2f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Apr 2026 23:16:17 GMT
LABEL org.opencontainers.image.authors=Alexey Shabalin <shaba@altlinux.org>,Nadezhda Fedorova <fedor@altlinux.org> org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 16 Apr 2026 23:16:17 GMT
ADD alt-p11-i586.tar.xz / # buildkit
# Thu, 16 Apr 2026 23:16:18 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 16 Apr 2026 23:16:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1676411b7009be50b237989080f5f14785db662ce1a94719d173f5a430270a90`  
		Last Modified: Thu, 16 Apr 2026 23:16:29 GMT  
		Size: 46.3 MB (46323048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a50c9f2a602b4e28e9ab62d9ddf1a7a8e620b82325e1fb6ff73b54d79a2fa4`  
		Last Modified: Thu, 16 Apr 2026 23:16:28 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:34b63853563ada98b6ae62c163571b03cadd6ff6c14fcc41a29a0cb939078199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b11c340ed504cf39e3abf25483369880bb82d54e49df4f3d1e1071b0fddbd62`

```dockerfile
```

-	Layers:
	-	`sha256:1c0c274d24b7aabb550fed0a5e45261f34e45616c7a2348f1c031c633efdd2de`  
		Last Modified: Thu, 16 Apr 2026 23:16:28 GMT  
		Size: 2.6 MB (2631042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5dadf4b05b7bbb45826166ec3fb86d3f4ebad9013d8da7a90f7d1f7807008a2`  
		Last Modified: Thu, 16 Apr 2026 23:16:28 GMT  
		Size: 6.4 KB (6366 bytes)  
		MIME: application/vnd.in-toto+json

## `alt:sisyphus`

```console
$ docker pull alt@sha256:2eee0cd037611c8292dc0af2a83054007b32dec2210ad56a3df89a6f266fae0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `alt:sisyphus` - linux; amd64

```console
$ docker pull alt@sha256:cf999cd1d08e56e22566416b5853c9642ad0b416c2a469abffd99cf4bd08c41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46671247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624ee8b67d720963ba05cbba24772d35cc9b86ccc5199dcb6aa8d298eba91a38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Apr 2026 23:15:21 GMT
LABEL org.opencontainers.image.authors=Alexey Shabalin <shaba@altlinux.org>,Nadezhda Fedorova <fedor@altlinux.org> org.opencontainers.image.licenses=GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 16 Apr 2026 23:15:21 GMT
ADD alt-sisyphus-x86_64.tar.xz / # buildkit
# Thu, 16 Apr 2026 23:15:21 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 16 Apr 2026 23:15:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1b5644609165ad036ef37371f0beaa3e2b26d406aa789d201e731a9b6a4ea69a`  
		Last Modified: Thu, 16 Apr 2026 23:15:32 GMT  
		Size: 46.7 MB (46671056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ee7ac6a4ecb2de839ac0e451349f43f854a4e97ec08279447e86ab1052f7d5`  
		Last Modified: Thu, 16 Apr 2026 23:15:30 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:c1cea715b465d08faab3a94d91c88607f851babdebb6a5e6c92bd326cb8bb458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2654788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948740c242db5a3cc8a51c344e59c5af5b5014de2629bc4a3c10ab6f124951b6`

```dockerfile
```

-	Layers:
	-	`sha256:17779ed4a366593489e4978f9527d8847b9d20e69821ebfbf7a86e3d6ec412b7`  
		Last Modified: Thu, 16 Apr 2026 23:15:31 GMT  
		Size: 2.6 MB (2648688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c6607e2d27a71c3904f4ecbdc2d3be1fc19ea3aea4904ba38b2ee9294f81cb7`  
		Last Modified: Thu, 16 Apr 2026 23:15:30 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:69a25ec1cb0e2b8379862d550045f2461bc2ee8992524df93e8a0cba5a540081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45365617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741807c2699cc0c9815228243dadb07dc8768efd8d9d89d777a828b28e8ea9ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Apr 2026 23:16:00 GMT
LABEL org.opencontainers.image.authors=Alexey Shabalin <shaba@altlinux.org>,Nadezhda Fedorova <fedor@altlinux.org> org.opencontainers.image.licenses=GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 16 Apr 2026 23:16:00 GMT
ADD alt-sisyphus-aarch64.tar.xz / # buildkit
# Thu, 16 Apr 2026 23:16:00 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 16 Apr 2026 23:16:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:75777fc776b0beceb2660d76442c5c89295cc37363f8b4be681a6c0272ae7fcb`  
		Last Modified: Thu, 16 Apr 2026 23:16:12 GMT  
		Size: 45.4 MB (45365425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b216283123311e4dc4c72b7792baadfeaccd864e9faf8b7d2a20c74724bff6a7`  
		Last Modified: Thu, 16 Apr 2026 23:16:11 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:ddf12fd15401c195e2babb4ab395657002d945384b2aa6180ad2224adab98c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2654251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7a25515414628d4181fdadcb3bed211a01fe1a327207e808499f09f62a9c2c`

```dockerfile
```

-	Layers:
	-	`sha256:7103b817dce6f00e69a54890bc1158106f89162e132396c9268d8ec885f3459a`  
		Last Modified: Thu, 16 Apr 2026 23:16:11 GMT  
		Size: 2.6 MB (2648105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ecdbd8059e7bc75ad08339c56274b37ecc2086fbd7f98303d6ffd8071874111`  
		Last Modified: Thu, 16 Apr 2026 23:16:11 GMT  
		Size: 6.1 KB (6146 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; 386

```console
$ docker pull alt@sha256:635394496fbee2229113497614a91cdfcc739def5ba407b91300739986ae5bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46671955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c291ed8cd8b982100e395e1d4445ea5dbaa66c8dccc315435798b8087b3fece9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Apr 2026 23:15:45 GMT
LABEL org.opencontainers.image.authors=Alexey Shabalin <shaba@altlinux.org>,Nadezhda Fedorova <fedor@altlinux.org> org.opencontainers.image.licenses=GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 16 Apr 2026 23:15:45 GMT
ADD alt-sisyphus-i586.tar.xz / # buildkit
# Thu, 16 Apr 2026 23:15:47 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 16 Apr 2026 23:15:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:84495811af3f80058c244a4853043768acd8765181997dcc7e6f1915e3e8ea4b`  
		Last Modified: Thu, 16 Apr 2026 23:16:00 GMT  
		Size: 46.7 MB (46671763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213baf35137df0a0362dd1d94e01d9598ba2a3b4eabc5ced476e5727a078320`  
		Last Modified: Thu, 16 Apr 2026 23:15:58 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:e4b893293b7016a9fb32da440bb282b96d7c5cb468cd9a8c74e64746488b0a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2653490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9181f57b295060edbf62fd0d45409b56db52c188eadeb1f7b145d73168c7c688`

```dockerfile
```

-	Layers:
	-	`sha256:a49782ec2281344fa032001e26ee139cda38fbae34a79cfa929a5ba10bbe94aa`  
		Last Modified: Thu, 16 Apr 2026 23:15:58 GMT  
		Size: 2.6 MB (2647414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5641ee5446e9350957e06d620c8973287079026300f2c46a122d4041dc1b13a5`  
		Last Modified: Thu, 16 Apr 2026 23:15:58 GMT  
		Size: 6.1 KB (6076 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; riscv64

```console
$ docker pull alt@sha256:3cf5bc6acfc8273dc2052faea43de4db6ad0007cd0cd63af5081bcc90e81332b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44486087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d2a588d57b588ae5273d2a515302542b60a3ceda71458c6a4f6c0e93075f90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Jan 2026 05:23:03 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Thu, 22 Jan 2026 05:23:03 GMT
LABEL org.opencontainers.image.licenses=GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 22 Jan 2026 05:23:03 GMT
ADD alt-sisyphus-riscv64.tar.xz / # buildkit
# Thu, 22 Jan 2026 05:23:04 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 22 Jan 2026 05:23:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ba25e668b40b2efaa9085cfdb237dd3fdac12bee44a47b6d0f8175d7c3eaa120`  
		Last Modified: Thu, 22 Jan 2026 05:24:49 GMT  
		Size: 44.5 MB (44485897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f644b3bca52aac38924d1e8d7515b0cb5ec91079fe48391b191fff649a9e5d`  
		Last Modified: Thu, 22 Jan 2026 05:24:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:52c85bd8165d1b5da180d18ce920bf9ce8a74fa34e27d1b515834cf7883c8a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2623698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18908b805353e0f803018b9e1dd6005bf5bd9b4b37efe28ddc7accfa6f6309bd`

```dockerfile
```

-	Layers:
	-	`sha256:7398354c4d28200d04aa4b30f5da872e5946e83d13d627671a9f01c40d73aa65`  
		Last Modified: Thu, 22 Jan 2026 05:24:42 GMT  
		Size: 2.6 MB (2617596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6598b1c5289c5c942753cee096d29bcbe5743711a88b57e9a06da50f3ed0ae98`  
		Last Modified: Thu, 22 Jan 2026 05:24:42 GMT  
		Size: 6.1 KB (6102 bytes)  
		MIME: application/vnd.in-toto+json
