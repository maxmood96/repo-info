## `debian:stable-backports`

```console
$ docker pull debian@sha256:c8ea95ed8ab3e5e202dde280b0a55d7bed48c5a509bb1285d044d7d2ea186b7c
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:10bcd19a2cf20c7894e476f6943b72893b9ba8ea13062ae15817a00ee1653bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49297756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65450a230ddfeec674b84d3ee6ebcbb451384e8cb36bdf916cfeb9f0d9fb4ce5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1773619200'
# Mon, 16 Mar 2026 22:16:21 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:27ff559a1e66012dca06c83b29b429e8606a0396b8ff007f64dcddfd72b5c507`  
		Last Modified: Mon, 16 Mar 2026 21:53:02 GMT  
		Size: 49.3 MB (49297535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617d78fc082b478829ce79ecc66b27593882d3c9ddb87b27284160fa845cf840`  
		Last Modified: Mon, 16 Mar 2026 22:16:27 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:cdb689dcc3c63be6a7ce9eb279892f24639e7cd715981d32094d73ac7cd9be49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c5aa892a9840be128fc891265824990e552e8107ea58103bb89f77825bfee1`

```dockerfile
```

-	Layers:
	-	`sha256:e68515e9c6de96302ff3576e5c2ea7fd379d3cd7d3ade74e64188935accf2b6a`  
		Last Modified: Mon, 16 Mar 2026 22:16:27 GMT  
		Size: 3.2 MB (3170913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e7f894f9217a31bf274d8525434090affd944f55d5875fbdd70488eb1eed569`  
		Last Modified: Mon, 16 Mar 2026 22:16:27 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:9d51c327e38a1a0a884d81a1142f422ec9ed5a81fba863202150d4482c2121fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47460830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7b351cba084b743484f3d84073a321f47dada5be0a605f280a84f23c759a37`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1773619200'
# Mon, 16 Mar 2026 22:15:41 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:baec035f8a0db7d20efc0df5deee85f22e09e27615f9fc89ee79cf8f414eb23b`  
		Last Modified: Mon, 16 Mar 2026 21:54:38 GMT  
		Size: 47.5 MB (47460608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557821192defe63efebf9ee5b6ae60777e7dc45e00f934f839b551e08806c522`  
		Last Modified: Mon, 16 Mar 2026 22:15:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c0c5a7b1524e0d4be66ed3e7325ff1ba077eba4e20d8dd0b3fe1c650ff801ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415309c0e164f6e6cbc548d597c01b30f49e06071caafec8b54f5dd40b72c7be`

```dockerfile
```

-	Layers:
	-	`sha256:bc3dcf248b814f2d39e1acdcc4756d3f89262a42d8d3e7e52a1c060787d049e7`  
		Last Modified: Mon, 16 Mar 2026 22:15:47 GMT  
		Size: 3.2 MB (3173850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18c1f6d226274439330b16ef6c296ecabcb952fd5590565ad5abbd62ca2ba6f0`  
		Last Modified: Mon, 16 Mar 2026 22:15:47 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:067244c3d68dc5f5bed56ace994978ada3f64ebdf32b7d497e16d77362c89cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45732872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8369d60759c0f0e8ca89d21b984baead8c549830a615e00b2d64a968f9bbedf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1773619200'
# Mon, 16 Mar 2026 22:17:43 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2fd5f0b05d440d2d9eebc85c966194f0ba100bc725ade4884898ae0d1daeb651`  
		Last Modified: Mon, 16 Mar 2026 21:53:11 GMT  
		Size: 45.7 MB (45732650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e1d29391804630f9132d5fc16f79d85f2ec5877cab00cf9af9ef6d2db5ebad`  
		Last Modified: Mon, 16 Mar 2026 22:17:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:412a8cad3c4f79407301e76af331e75557d5a39b63affbff4f178ec519b65294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16651f69bed5b7853629f9e980215af1a4effe56a653e973e342b2a9114b0640`

```dockerfile
```

-	Layers:
	-	`sha256:114fb455f11d2ec4eaf2cc5cea61168d5c7e892b2a161fed0543674d02eb1cde`  
		Last Modified: Mon, 16 Mar 2026 22:17:50 GMT  
		Size: 3.2 MB (3172287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:896ffcb554e726b26a1d08263d98f7c7569d234a4214db5f269397ba9b78dbc8`  
		Last Modified: Mon, 16 Mar 2026 22:17:49 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:77412aa04762139f4bd82111d65883ffdfc588ba2fbf48567ce74d9593cf2bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49665178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b60e62b63cbb0b09bc020520cb0d36fbca94656b250c2b9d8355768e89f9d15`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1773619200'
# Mon, 16 Mar 2026 22:15:46 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ef357e30c2dc5bd251791d06a9e7f9d99f050c0042c9772752847145d6402b65`  
		Last Modified: Mon, 16 Mar 2026 21:52:37 GMT  
		Size: 49.7 MB (49664956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ced7ec14da9626948dee41a3f907c755dc3930e13a1b5b5d8f282d2e14b3f0`  
		Last Modified: Mon, 16 Mar 2026 22:15:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ec298c758825c720288e33b192771abe97934a00b13a998f78d8e13a92079e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf832b535b1a9f67b31ddffec97c4ffd3017c0ab388dcba3a2d658b5261dc10b`

```dockerfile
```

-	Layers:
	-	`sha256:738d0b6e3d4e80feca18be2e8109c9aeb1263653061507a80b0a7e8e8e0bff90`  
		Last Modified: Mon, 16 Mar 2026 22:15:52 GMT  
		Size: 3.2 MB (3172394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b9c494dd44c2c4b364c5e8734658063a1ff6b2ce5e454b5a42d58b6b51bf5f9`  
		Last Modified: Mon, 16 Mar 2026 22:15:52 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:33fd1701470448daa0acd63e7100327f225930f867a9647847edc0dbe82c3196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50819012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4440292d528be4a556a865f1a3ae12759825d1ca2626e0cf01b88ed11c993615`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1773619200'
# Mon, 16 Mar 2026 22:16:17 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bd2ee5730f15d6320f55605b391381db5c0db6fc3b4351e4bc467f76c37456d2`  
		Last Modified: Mon, 16 Mar 2026 21:53:25 GMT  
		Size: 50.8 MB (50818790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03549225c552d99829e9b0128c04e108b3e44996c3b20ebc0a8fa2fb4fe5d71c`  
		Last Modified: Mon, 16 Mar 2026 22:16:23 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:46987b9e4c9dfb0f8087ab0a11f3ef686198713b4ab75ce059ba6dd2a90d9aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a8a58384d19ef3b6bd8a2a5c7cd12c30d903d5fa1ecd3ed1fedee8d7fc7dff`

```dockerfile
```

-	Layers:
	-	`sha256:5c7e0a594a79fa261872b58934628aa210eb7e8279f2bc9f55d9320617d488d5`  
		Last Modified: Mon, 16 Mar 2026 22:16:24 GMT  
		Size: 3.2 MB (3168115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cb9984ec011d72b1e0f15ccc129157f85e06d27da74a2d49c7e388d81a9787a`  
		Last Modified: Mon, 16 Mar 2026 22:16:23 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:647d783ad671ddfa87512462ce6d5ddee52df5b2a0f1182f9e9554aca310938b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53112485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd91f0c54a95a5c28194aad8b7a5fb8c579e69e95424cadbdafbfa4301d26ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1771804800'
# Tue, 24 Feb 2026 18:54:02 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3bde950ce93c7536badd86576e1b614d13001c4e8b0acc9190a6a7c6bc64894e`  
		Last Modified: Tue, 24 Feb 2026 18:44:08 GMT  
		Size: 53.1 MB (53112262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce64370d038f44de3e4b91eed4111d3885a31e7a3daba2033f3aa42e3d6b68b`  
		Last Modified: Tue, 24 Feb 2026 18:54:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:134ce461f03ce09f39a4d499fb96b86e92202e8f07abc496e8f16ac81fd73aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3846a5501ceded704969d8ae0a0ecb43d655a3c5a9004162578bc443dcc27b`

```dockerfile
```

-	Layers:
	-	`sha256:143a9d8772cb736afd9bc3c01f2842968361df89db310879f85494644660f386`  
		Last Modified: Tue, 24 Feb 2026 18:54:21 GMT  
		Size: 3.2 MB (3174390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:666a7af75411f2b9a8d758ffd307a5de3dc929e8b28f2f09729767a918854191`  
		Last Modified: Tue, 24 Feb 2026 18:54:20 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:a9d9bcb5f3019e89236a470ac6cb25234597f3788f88133c66cdbfbaab984f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47792547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0e449c65010650ac445a397ff6185dd8d18fafb493cf6339713d404e57dc3e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1773619200'
# Mon, 16 Mar 2026 22:20:58 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:81b160e90206e6d80439893bd60b0ddeb3ac52a36c7d6772a24871dd9a8ce145`  
		Last Modified: Mon, 16 Mar 2026 22:02:21 GMT  
		Size: 47.8 MB (47792325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81745528357b9ab5d5d911f069df824aa94203713b61f0889454e38a80d488c6`  
		Last Modified: Mon, 16 Mar 2026 22:21:50 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e2ccccabf22f2ebf10fd3ef32bf67fe82464eab394e32ed957ec98e9963d1d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfb5a28b9b0d8e2e9816c43f50ee17a4f123ebbc6fa57d8e29b62ca6e45bc16`

```dockerfile
```

-	Layers:
	-	`sha256:6c6de97dc492168d3827ba67abef92b40c6b2ad9831dc3de94e71a6c56e6c5a5`  
		Last Modified: Mon, 16 Mar 2026 22:21:51 GMT  
		Size: 3.2 MB (3163238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2e760b76c00e4a6a1128092a1c84186aca9aa434833142afabef0d38ae729ff`  
		Last Modified: Mon, 16 Mar 2026 22:21:50 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:fd3d315812c05e5b592037ebb523258724036931f092cd4f47a104d9b4c1d8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49364995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd6673ef9665a14df2bb5306fbe7bc22022d0e24083814e1c2159e697056af4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1773619200'
# Mon, 16 Mar 2026 22:14:56 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c8697a3146d8e76721353163a55eadfeab5a454ef054a29cf671b389ad5e353d`  
		Last Modified: Mon, 16 Mar 2026 21:52:25 GMT  
		Size: 49.4 MB (49364773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56e50684b9b2a4e5131e597d87d423a40f539bee3335ef414919c01f33c3261`  
		Last Modified: Mon, 16 Mar 2026 22:15:07 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ed2cdbec1846179d55f32ae651818ce048a2ea0222a946b33399da0a874b649b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe1d461663e13a43bea11153bd32de6c597ead67003dadc55ad38f37c76faa6`

```dockerfile
```

-	Layers:
	-	`sha256:bf6f6e8152d58efe58bb6da4e27bb69af45bc83b9782924befe0ebdc6a219713`  
		Last Modified: Mon, 16 Mar 2026 22:15:07 GMT  
		Size: 3.2 MB (3172360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c18fa558ace425a431f65b05ac165a98ebfcb8cfb05a66b2116abdf442e413f5`  
		Last Modified: Mon, 16 Mar 2026 22:15:07 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
