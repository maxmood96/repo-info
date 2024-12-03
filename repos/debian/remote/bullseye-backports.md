## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:8025a06bb77c4d58d3522afb68cde538f59296f5ef0efee83cdd170ba298cf8c
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
$ docker pull debian@sha256:c3ea17351bfa2367df7d01098d51d79d3590f6b9e43caeb4fbd70d21998a2f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53739372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033b7cecc2a93431af877952267cbff91ec5e8cf961b964d235329fb74bb1a42`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d244007ffa861a6a71947b31223454ba48ed0e91ff7e1fd4c24a9292b4f5e8b9`  
		Last Modified: Tue, 03 Dec 2024 02:13:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d03197e158c071abf8349ee629353018905b3cb39cfed00dd4c59e5b33575fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3927856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0e1b674a6a8ad7ef744b1e132ad233d63dd0a0693b5ed347a4a7b84df5882a`

```dockerfile
```

-	Layers:
	-	`sha256:60c634f2341e26540ebdadc3df00160fee8953a23b9b07bbd488d17c71696b6f`  
		Last Modified: Tue, 03 Dec 2024 02:13:53 GMT  
		Size: 3.9 MB (3922009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:961e0f6c0c1d64cceb357bd6ff3e2c78af29190653659663b2a9b3a16920859c`  
		Last Modified: Tue, 03 Dec 2024 02:13:52 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:76a3b27fd44e01006e0af629eb20f8810e26f10ca952be611a8ba0adc013a36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49025246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a99f5da7054aa55b1411b2e8b6a9aaae553af4a76ba751ce553e2797542dd43`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:69dbedc8019388fd330866fcfa04c35d28f86d1ef986691ee290054433639992`  
		Last Modified: Tue, 03 Dec 2024 01:28:37 GMT  
		Size: 49.0 MB (49025021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b807492ae60651100e80b822728fa4689ed2eedf3b6d7d9a5b8b2c2691c80903`  
		Last Modified: Tue, 03 Dec 2024 02:19:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1e86806407b5e966e98375f86fea8b77ff4da2b59cc6b892a6fd9624cf93e33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1d117255bc76b18873ec60590c246738b3c544e0fb656045d2cd6c5472df44`

```dockerfile
```

-	Layers:
	-	`sha256:e972d2355904fd5bacad0318bf266de1ae7d363bced1324f59c739b50aa226f4`  
		Last Modified: Tue, 03 Dec 2024 02:19:07 GMT  
		Size: 3.9 MB (3923569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7719390ffaf53ae0c4e42df3b13c348b9ddb5988285a7a2cd25ffd021417f98`  
		Last Modified: Tue, 03 Dec 2024 02:19:07 GMT  
		Size: 5.9 KB (5898 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d64484d2a8434c9bc5019d7ef3fc2d0118a119a043bf4167190eb58f7692f065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52246220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c0071730b98162a1de59f9253c191d78592c5001ca9927812bec1d8cd35539`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d433fc18ed286c5b77aba9dde06c1d509ec5fedd2c038988b7dde5f799c5b2`  
		Last Modified: Tue, 03 Dec 2024 02:18:32 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ef3af8ad295ff60423cf62826f01edbecad21066e2b689f6a64d229ef97c292a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3927502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41effd98eefe1da49d8d465e2efa6e0b6e19bb35bf2fcfc46994d9f72d4f4cf`

```dockerfile
```

-	Layers:
	-	`sha256:b30317d979993b37a1a9160f6d903f5c7c6a17decdc8753108b6a72c0f98326c`  
		Last Modified: Tue, 03 Dec 2024 02:18:33 GMT  
		Size: 3.9 MB (3921587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b82817147ead89afb5ffe84f6588641f8b6775a2595e334f04d14f26e03ed494`  
		Last Modified: Tue, 03 Dec 2024 02:18:32 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:0742425ab27a96aae2b1a6606095d7c63112afef8abcb79dc3ce4275b1badce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54676500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7131c2bbae9e11b7ca5a496191fe82f9d0a2d988d0ed54563c0438d5b0e17f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Mon, 02 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:862f429b4105c1e5714d48631896837c3ca6f797479296293b7c33c6699eae95`  
		Last Modified: Tue, 03 Dec 2024 01:27:25 GMT  
		Size: 54.7 MB (54676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d8f63b96e7b7ed0b56c330c5ad9be40d32383416f788c010cb2c3d7fc7c4c7`  
		Last Modified: Tue, 03 Dec 2024 02:13:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:dd4f00543ba683dafe680731838bb64610081c0182d3e762f6e775b686bd8ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2aedeceb34204cebf1995079fdda31fef26653d12df20743424428be43172a`

```dockerfile
```

-	Layers:
	-	`sha256:5ccf55083d8d1cc21fcb9895f1250b4834872994536e2fab490fb2bcd219ac4d`  
		Last Modified: Tue, 03 Dec 2024 02:13:50 GMT  
		Size: 3.9 MB (3918514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfc2953b90759314e7f0defc21e0273b24bbe0cbb1000e252462e8ff18e85cb`  
		Last Modified: Tue, 03 Dec 2024 02:13:50 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json
