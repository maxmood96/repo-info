## `debian:stable-backports`

```console
$ docker pull debian@sha256:d7b48b3dd3261e8ebb265f49395bd0256ecc8c197da00bbe175bb8dff5aabfe8
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:b6c54c1ec66b53b5748dcf58fbddb0cf78fd7029f921a6e046d1ce3d1e432655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48480187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ea94646d2033c7ccc2f677e6015c1ce50259707c81ce56825188f805d733b6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4ebd30dde7969de84afae49eebe28c2933fca00588db643bd41d74946d2817e6`  
		Last Modified: Tue, 14 Jan 2025 20:33:36 GMT  
		Size: 48.5 MB (48479964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b924f953a26a78a80110c3d30eed542083433b21018d83c732d568ea56282`  
		Last Modified: Tue, 14 Jan 2025 02:15:37 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:afcab30224b4924fc84d2241b0c89956be0dcaeb9612f8066d4041d9a52e73dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6091cb54bb388864bd22258c64c5cbc2038240506fe1c9dc6396be29cd242a24`

```dockerfile
```

-	Layers:
	-	`sha256:2545fd26f6b21a3620fcaa0763f39db814f18a32e4d1cc0b85432af682c044f6`  
		Last Modified: Tue, 14 Jan 2025 02:15:37 GMT  
		Size: 3.6 MB (3619206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b0a940abfceac3851ceface6039f6fd4ce7af0c392c1190eb0b02636d64cef8`  
		Last Modified: Tue, 14 Jan 2025 02:15:37 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8108701b56c3fd813424c627493fb83008c03f73badec8744da65872d92363a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46007033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cdd85daaf9bca3398db43f6c6810ac4abc7a3b4e811252afe6baddd91edb565`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f3f4b2dfbf46a72241b9e5f62c5a67a9da20c8f924fdf44ba85bf372989343c3`  
		Last Modified: Tue, 14 Jan 2025 20:33:51 GMT  
		Size: 46.0 MB (46006811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d992881ba1ce2f712c831bab4d5db25a47563f83aed1fe1cc38deb882f678ac0`  
		Last Modified: Tue, 14 Jan 2025 02:16:25 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:96093c50a13bd16e6a4a729ed631849104586e4667fd9609e41e406f7b0a3be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3452a48092c65126fcb348c53a0d504e54cad289e248e5b71f2a65c649fc009f`

```dockerfile
```

-	Layers:
	-	`sha256:530e8fc8643e30e3b350ba46fbaf19b4c1463e917fb1d9208786c1f055814b48`  
		Last Modified: Tue, 14 Jan 2025 02:16:25 GMT  
		Size: 3.6 MB (3619407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2066a41e649e4089ad0e32c9cefcb6c09dc54695661ef86208c22cd55ebe73f7`  
		Last Modified: Tue, 14 Jan 2025 02:16:25 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5fa2b6cc717960ada3554d2d7484d6e151aff8db81f005f2a914c7ec8a84e44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44184429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f94c688971413789a6d382b64feaa63aa7e67c21ea54a826a4242d38dd3043`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e7dd4633c23b81448dfd41780be338f85e6ee2c474d7317406828ebeb648742e`  
		Last Modified: Tue, 14 Jan 2025 21:40:46 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dbc84d382fbf0833b95538b27b2cdef50efbec1a8e0cb50b2cf0fe0b684049`  
		Last Modified: Tue, 14 Jan 2025 02:18:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fb2a10bd8f04c15ab5bdca47db3c27294ed3a1ef7b7f5d099a17cb96c931d83e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48043483ae575196f52c495a5030780c2f6639952fbd488449ecf963e6084ff7`

```dockerfile
```

-	Layers:
	-	`sha256:d8ef53656c41968792f2cd60cbbae17ba03a89c49d37e6f571a2c47d36ed1a0f`  
		Last Modified: Tue, 14 Jan 2025 02:18:19 GMT  
		Size: 3.6 MB (3621385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3f3c2551cb247ed31b14de1596625270a6db9207c17a6dbb92c0cee666c605f`  
		Last Modified: Tue, 14 Jan 2025 02:18:19 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:9c58e7ed54af0484776e31c853eeb4fc4a91e8f5a2e761339b2a108f26fbe643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48307114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f72eb1f79d430463b20ce4b27dd82a10a7ba7bfaba3ba947d4a9a2332ce97e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9c6d27747aa6d82a5cb1ff7b82128b17e5ec79286a33dbb3c0c8f61e386a10b1`  
		Last Modified: Tue, 14 Jan 2025 20:43:51 GMT  
		Size: 48.3 MB (48306893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd968fa611286c936f1ff22970ae54673d13201affc1cc2006ffb49312e4638c`  
		Last Modified: Tue, 14 Jan 2025 22:04:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:538fbcf3f888f0a2632c6b99454a547d53fc597e90ec9f367ad754f7764874b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40963880c1aba6c8c6a743765cc98b65a5570d5d0ff1fd4fc903e2b98f8b2c82`

```dockerfile
```

-	Layers:
	-	`sha256:18e20a89175cf31a0a54e4bd94a49e8ed6b237835548a60f8d8787c8bb4f18e8`  
		Last Modified: Tue, 14 Jan 2025 02:23:38 GMT  
		Size: 3.6 MB (3619421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0778a8bb4c438abd8525f17e192c0b77540293b8d5d1cb81276b253028c844b`  
		Last Modified: Tue, 14 Jan 2025 02:23:37 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:96bec2160414af774b65a95b85e652d2a7006fe9f6c7fafc24453af5fd72f159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49457964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a79e89398d2e2a013549c520ef78be7c15c2c4b0c2feb832fcc3942eaaf5ad0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4aba00288acedd5a160b96e675cf6bebbdf5679b74ada3c8078270ef9c250f7b`  
		Last Modified: Tue, 14 Jan 2025 20:34:21 GMT  
		Size: 49.5 MB (49457742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2eb8521f4e39395f9faedd6e491e7413182aa79acc388b02a64f26ad5f26a96`  
		Last Modified: Tue, 14 Jan 2025 02:15:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:60166a92b3f4244c96a6a8b37742b9c1f014ae970f5105352ad1fdc4ef41879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1fd37b212118449eac9c8df768a83f25adf65765b43fd4d6b123e24f21e7e97`

```dockerfile
```

-	Layers:
	-	`sha256:d1615df9309890acb6f63551a489166bc6ce69fe996ce49fb883d36aa6f8589c`  
		Last Modified: Tue, 14 Jan 2025 02:15:41 GMT  
		Size: 3.6 MB (3616367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8136dcfa36a2fd793d93edc578844916dc02ac3d5b29659b4c219c199b20a081`  
		Last Modified: Tue, 14 Jan 2025 02:15:41 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:9ef371be1c3e003068ad2193893ca08e51d3c290de99e22a0d09a4846bb2766b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48758321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70cef2188303d7ec230021dc86d50bab506bbe0c64f5232ed3636eece17e920`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'stable' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b16523ff5f677c13645f66ea4afac964fc070b8cde74e0155bee8f02d4d945be`  
		Last Modified: Tue, 14 Jan 2025 01:35:57 GMT  
		Size: 48.8 MB (48758100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2111f7b4e97900abdf748deebacbc4aa911af8a3afd39823b5e8791e22611915`  
		Last Modified: Tue, 14 Jan 2025 02:18:08 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b8cf3800bbfc3562b08560e9126ce93b86273a8bbd8bccf2e35bedaa06800abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b89c061453330c4968464e719e09cf12eddc25b6afa5d167f01d96f827596d`

```dockerfile
```

-	Layers:
	-	`sha256:ad857c0a98877832426947c6d36fc34349aaebc0485f3e5de91282f333d7c37c`  
		Last Modified: Tue, 14 Jan 2025 02:18:08 GMT  
		Size: 5.7 KB (5651 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:d73e41299e1c7bebc9adcec7dd81131e0019dad56126a56c5a0713a2779336e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52313364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5019ba2e8446d6b1d7a74aca7cfcf109f87a9bf31bc1ac7f9b0873dd00bb3b50`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f70b1846320f9401a1d01af994d055f3624b05b1e70b74c0a88dc6dd4ee40970`  
		Last Modified: Tue, 14 Jan 2025 01:39:00 GMT  
		Size: 52.3 MB (52313141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7370937857453ed0769bb5dfa44b2b9c8b90e163986dacb4461d7887a2dac37`  
		Last Modified: Tue, 14 Jan 2025 02:38:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d432a4f8ba45d8f04d4a30d31e4bcc3ae220c0c1ff60e56725203e2857d7d08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aba8fb5421f6423947b1c0715c450e85f3b422138c499339945bc8439422e24`

```dockerfile
```

-	Layers:
	-	`sha256:5930442ffb7ca2745a298a43b3552b5bb5221169cbcd2e0c95f6ab3b1ce5e778`  
		Last Modified: Tue, 14 Jan 2025 02:38:27 GMT  
		Size: 3.6 MB (3623466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4dde10ab1317114077bbd63669ec7637c6b63d6f67fa70d19e2b544ff2013a5`  
		Last Modified: Tue, 14 Jan 2025 02:38:27 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:9b922d62b2f1dbb287395d1351ab0674daf3d717c2ca434e42f9ea613fd63a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47132006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b113b4a19cedcc34817bb759f2a0783e9957cff10bd3ff5b53229cb5517d7236`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:eee134c4539343d043bd1d28c58b200e25e3feafdc513946091c137de70b976a`  
		Last Modified: Tue, 14 Jan 2025 01:36:31 GMT  
		Size: 47.1 MB (47131785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddde7ed49e9bbe71022b06743929f4484ed8e74cf6760ea9e7d935f92acb11ab`  
		Last Modified: Tue, 14 Jan 2025 02:28:46 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:290c8ef8b4241324254e265c5ba1101367d08762142bf1df645820dc0a85b384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3624763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817e5793376b43eac2f7d7bb622400c10524fe4bcc4f1f8857f2ebd567a1a54d`

```dockerfile
```

-	Layers:
	-	`sha256:d81c0481226773d9b5128f52966ca2962507022e7b34ecf24a12d2587bacfcc0`  
		Last Modified: Tue, 14 Jan 2025 02:28:46 GMT  
		Size: 3.6 MB (3618936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16ded04082c5d5902887accd3597b5cf58cccd9386d8b07619a3f7db25f24371`  
		Last Modified: Tue, 14 Jan 2025 02:28:46 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
