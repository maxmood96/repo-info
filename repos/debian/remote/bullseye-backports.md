## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:f8bbbb81ed0fe0af14d7f5f141cb9bd94265ac33401b5a639fe5d0bf36862b77
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:60d426b6ee47abb8ab20e1bec10a3869c6f8947a5e1a189e5f9778a07184a76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53739388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a460b0d344333a41f3bdc125ab40a8582735b5048fbd5245b9cacd00add9cffa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e65f7eb478ae0f3c96c7ccf19010ee38bdf66fe7cad2fe91eae575c6ea8a7d`  
		Last Modified: Tue, 14 Jan 2025 02:15:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:cceeab689026654fb22e8f307b5a16b4bd33ce660f17340533be627a087149c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43c5acd16d3f7d50b85896e1e6d54b631631ef38fdc985333097fda7edc8af5`

```dockerfile
```

-	Layers:
	-	`sha256:e699983a92d95d5d9ecb62c40face88f8526290c01f3d02e95c4216bf5fd1cf0`  
		Last Modified: Tue, 14 Jan 2025 02:15:32 GMT  
		Size: 3.9 MB (3917516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c640faa70f102edb09f812d8db74a5df8373cdff210ba7259338a80918bb4a00`  
		Last Modified: Tue, 14 Jan 2025 02:15:32 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:3492a74643f8fafc27cb5fda40e66b4401d8d1e9ec49932688a5f3570cbac386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49025286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e51a3c75e5cf0a905994e5ae089724aa5650cd7102bac47d482144080c10847`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724245799af1a14540c866a116944f804013af69d7cdbb1f515ead8ee43def92`  
		Last Modified: Tue, 14 Jan 2025 02:17:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:67e222fa52ac85672d6a3124544c233d91ecff2468d9af80a927cc96bd5cc504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f50208defef9d20a624bff3846b07b473d8d06518495b9e4f0afa07074d69d`

```dockerfile
```

-	Layers:
	-	`sha256:3946a5610fc1851dd4c906b6bd37c4385f27211913e13eb05b569cfcf1e24ee7`  
		Last Modified: Tue, 14 Jan 2025 02:17:30 GMT  
		Size: 3.9 MB (3919078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a84f7c791f906ceb94f75d6da91368ac4689d147ceb9e4cc1fd00937b9c38ef`  
		Last Modified: Tue, 14 Jan 2025 02:17:30 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ff4adc53a77567752ef7e669ca0caef957c47ee7eddc41c3da239d36727dda8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52246285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e025728f8639a6b442877b2e49c3cd10051b11982ba70fb69c84ebba9e0e5240`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d11e711650ba9aa1c28c816b21ab6622b5b0d0195cfde79c9a687e6974c10f`  
		Last Modified: Tue, 14 Jan 2025 02:22:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1f25ece5ee76c621e0aec04887fb04995ec9ad75d08ea1de617176407e2368d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de021ededcf4c7cf591eb2692789be651ab2a7b1cc80740642137de1a8639bb`

```dockerfile
```

-	Layers:
	-	`sha256:62875a4ac5a6d518bad84583ea09df458082c5fc12ded8702bedae6eb9054185`  
		Last Modified: Tue, 14 Jan 2025 02:22:35 GMT  
		Size: 3.9 MB (3917096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a46cd6b7c9c4bb856c62e17cf8148dc70669ed6077dfe802c8833d1e1dcacc5`  
		Last Modified: Tue, 14 Jan 2025 02:22:35 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:416166ac3282d1f70a6b824fb66182b8e0bcb9fcd64d44b9258e79908a8c35c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54676501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab0ee7146209670295f857b27f889e32216ba4b379d2fa598b0a6117bd67347`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b72c0b254e0d45985d121f47650a88f2ee35fbb4ff596c396ee98094e0a26d1b`  
		Last Modified: Tue, 14 Jan 2025 01:33:19 GMT  
		Size: 54.7 MB (54676276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8b249484c10ed056c1dafb8ccbd6bdbd58241ea88fbdfa904a207527ef6f84`  
		Last Modified: Tue, 14 Jan 2025 02:15:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:466c8449649ce572274c1ade1c8c11e8829652f0ee74e1d4ab18d7d6c8f3dc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b613cb150491deade1959cffbadfd62eb399e49e478be2bb22f268144901e9a`

```dockerfile
```

-	Layers:
	-	`sha256:76874deb7208af9e5dc1976f7d45b7ba1b01c4e325d3e192d0d6acc72d06ba9a`  
		Last Modified: Tue, 14 Jan 2025 02:15:56 GMT  
		Size: 3.9 MB (3914023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53e3a2348401d9cace91191dc9c30429a49ea3ee46c03f48f1c5386458dd8a22`  
		Last Modified: Tue, 14 Jan 2025 02:15:55 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json
