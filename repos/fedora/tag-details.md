<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fedora`

-	[`fedora:39`](#fedora39)
-	[`fedora:40`](#fedora40)
-	[`fedora:41`](#fedora41)
-	[`fedora:42`](#fedora42)
-	[`fedora:latest`](#fedoralatest)
-	[`fedora:rawhide`](#fedorarawhide)

## `fedora:39`

```console
$ docker pull fedora@sha256:d63d63fe593749a5e8dbc8152427d40bbe0ece53d884e00e5f3b44859efa5077
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fedora:39` - linux; amd64

```console
$ docker pull fedora@sha256:2c060df36801d0b1c616ec5e0dcb79f0513b8ee245d9629d033c40e698cfa809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64950404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f29760e1bf258d128a684e79be7b80eb394f4067fe012d7446e84b39960c1d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:45:47 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:45:47 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Thu, 31 Oct 2024 11:45:47 GMT
ADD fedora-39-x86_64.tar.xz / # buildkit
# Thu, 31 Oct 2024 11:45:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c6321f3889d450dcf0c3bd9dcccf322a20dc351997ef7bd4261de4796b551d4`  
		Last Modified: Thu, 31 Oct 2024 22:59:40 GMT  
		Size: 65.0 MB (64950404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:39` - unknown; unknown

```console
$ docker pull fedora@sha256:0e2db70ad704877f545a9011344022eeeb1bde90c57e700bbedb380361eacb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4391574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02bf33d32f1ce9bdaee6ece1d2b3bcd948aee88e4686195485a3da315c5f543`

```dockerfile
```

-	Layers:
	-	`sha256:ec3db909f62b9ecf6c4d14be9b2e541543b1d82b76dab7305fc0d44eaf0f8d72`  
		Last Modified: Thu, 31 Oct 2024 22:59:37 GMT  
		Size: 4.4 MB (4386615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57b54c94ca36bed486f0ec80242346745a7cca986cc2dd73b91045fa84de7d76`  
		Last Modified: Thu, 31 Oct 2024 22:59:37 GMT  
		Size: 5.0 KB (4959 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:39` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:f4adbb590dc7be8d73a7c19934260270a143e86db970046f086ac9a130f5ee43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63603983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5245a3ed2cb0b4163115866167ce44c9be6f82993751af7008e82ee76c1895`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:45:47 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:45:47 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Thu, 31 Oct 2024 11:45:47 GMT
ADD fedora-39-aarch64.tar.xz / # buildkit
# Thu, 31 Oct 2024 11:45:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:95ad4e12c6a70725237ec9cacfc6f349be012127972c8202b7593ba8ccbf7304`  
		Last Modified: Thu, 31 Oct 2024 22:59:18 GMT  
		Size: 63.6 MB (63603983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:39` - unknown; unknown

```console
$ docker pull fedora@sha256:d13f9e766b6b0889c7da627955ce28867c32a9b45c64a97e5fa3303db1790557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4391693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83d15b767dfe55294a05f85501d94ba80a59d62b447bcdefdbd38e7393b85d7`

```dockerfile
```

-	Layers:
	-	`sha256:d2a0d8635bff8afe99b22245130f586b159959cf27a8a94ebccd1e69f63fcf2e`  
		Last Modified: Thu, 31 Oct 2024 22:59:16 GMT  
		Size: 4.4 MB (4386702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1738bb91e4e1a6a78b36fc54f0b5139bee6b4dea940cb11f793e514d4bcf8136`  
		Last Modified: Thu, 31 Oct 2024 22:59:15 GMT  
		Size: 5.0 KB (4991 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:39` - linux; ppc64le

```console
$ docker pull fedora@sha256:7bb049e163ab5ff3aa8eb0f6782c3f8477f75300771f1d68d6305e264c8e2431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71611844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cac7ce83e6b96123af07c4fa07b3f86367ecf78b1aa3c51f6b409823971f916`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:45:47 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:45:47 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Thu, 31 Oct 2024 11:45:47 GMT
ADD fedora-39-ppc64le.tar.xz / # buildkit
# Thu, 31 Oct 2024 11:45:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c6d062d5e8bb8f72dbfc5639cceb1f8a94d3d2c38a8f82ff904e7562708eba0b`  
		Last Modified: Thu, 31 Oct 2024 22:59:46 GMT  
		Size: 71.6 MB (71611844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:39` - unknown; unknown

```console
$ docker pull fedora@sha256:c0d3a9d870397507998a791b6173a5f60f240bad7f62a0a7f7da833d34bdfc65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4391328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060bfd41ef2e9dd8951c0c07a4260eb1c84c8fc94c4f7f34ba6e0e08557bf1ed`

```dockerfile
```

-	Layers:
	-	`sha256:e319ed391a41de2cbc526bc5494306d4e7fa9dc3228c372715dc19eabfb4d497`  
		Last Modified: Thu, 31 Oct 2024 22:59:44 GMT  
		Size: 4.4 MB (4386350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c8d7f9ee263506ddd66c8b2e4d73352f8593553d85fdc232366aa1d2ceb4ec9`  
		Last Modified: Wed, 08 Jan 2025 03:31:03 GMT  
		Size: 5.0 KB (4978 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:39` - linux; s390x

```console
$ docker pull fedora@sha256:42bef5dae397f34b87e5b13b15b6403398e15dc6de9cab0447ad1940be2d1cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65506247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e65b5d14b786c6a730c8286c10e69975136f1d742cc1d9b08e274eaeb5e801`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:45:47 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:45:47 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Thu, 31 Oct 2024 11:45:47 GMT
ADD fedora-39-s390x.tar.xz / # buildkit
# Thu, 31 Oct 2024 11:45:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4c6db063e248756fd3fba18e1e34c218ae8ff7e522fa9728bc862d238d6c0975`  
		Last Modified: Thu, 31 Oct 2024 22:59:29 GMT  
		Size: 65.5 MB (65506247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:39` - unknown; unknown

```console
$ docker pull fedora@sha256:7a8f1be78dc17962a41629ada1d4b1db298d422d2945f4a849c8a9101614a947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4394005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32726848adc7bbaeb4fb6a266ca8aca31f7508ee55d248c808aedd1724054b0`

```dockerfile
```

-	Layers:
	-	`sha256:66defd1ffb852516012e7f2e254dbf16eee15531e548c2fd39c6e62e244661a8`  
		Last Modified: Thu, 31 Oct 2024 22:59:28 GMT  
		Size: 4.4 MB (4389051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce91027b15673345c49bd6d9cfcd8bcf4cd71f560bde450817c5a512cc5efd0a`  
		Last Modified: Thu, 31 Oct 2024 22:59:28 GMT  
		Size: 5.0 KB (4954 bytes)  
		MIME: application/vnd.in-toto+json

## `fedora:40`

```console
$ docker pull fedora@sha256:7cdd2b48396929bb8723ea2fa60e03bee39cc22e2a853cbd891587fab4eb1bc9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fedora:40` - linux; amd64

```console
$ docker pull fedora@sha256:0dc52447068058c56588a816d43bd80d4279dcbefbb74f2aa55d2745413afbc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81085828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04236519bb70082cc87116ed04d3e194c1346d82fa6aed987e64c7876638166d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:31 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:31 GMT
ENV DISTTAG=f40container FGC=f40 FBR=f40
# Thu, 31 Oct 2024 11:44:31 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6299667869c403ec0a090b3a89b996709a97f5fd524aef791d490952b92258bc`  
		Last Modified: Thu, 31 Oct 2024 07:45:02 GMT  
		Size: 81.1 MB (81085828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:40` - unknown; unknown

```console
$ docker pull fedora@sha256:693cf264179118dccd5f6c84ca2a04ec5730de2ce31e9cee025947953860ee09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa8552bd06a61376fd3b86d32e2b51bbb64df075aafb7c917659b3b29528c4d`

```dockerfile
```

-	Layers:
	-	`sha256:9e93b3b98afd937f9c85f9189cb3a2a9d488a90a91ccbe35d0a1fb0f7d5d6d67`  
		Last Modified: Thu, 31 Oct 2024 22:59:37 GMT  
		Size: 5.1 MB (5101344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3c1ce7520c2388c4fcd6129fbefac1438de222fb253ac6ff51f2761539d6fd3`  
		Last Modified: Thu, 31 Oct 2024 22:59:36 GMT  
		Size: 5.0 KB (4988 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:40` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:97b4eb8354315e562641463bfa627a3d8e9af8d692ae32c432b2a224f340fb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80932206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e5d3f1cb6ad864518937faaca74d1d79f43012c9be83255400e4438b72c746`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:31 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:31 GMT
ENV DISTTAG=f40container FGC=f40 FBR=f40
# Thu, 31 Oct 2024 11:44:31 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6405a3879f35f2a3caf1ce3e9bd05983ba7c5617b1ac277d5664f64e2bce4e0c`  
		Last Modified: Thu, 31 Oct 2024 23:01:06 GMT  
		Size: 80.9 MB (80932206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:40` - unknown; unknown

```console
$ docker pull fedora@sha256:87753ff14c6bcf349f0e920bee06f07ce4671604e447dc9f4cf8c32fb29b321b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd08308aa207e4906020b0065b6b636af29471172d5ffe0394dcb8c3fea4039`

```dockerfile
```

-	Layers:
	-	`sha256:3071b362f1ed1c61b6bced5c7d94c41577daa7f51b4dfbdac1eab762656b1e39`  
		Last Modified: Thu, 31 Oct 2024 23:01:04 GMT  
		Size: 5.1 MB (5101431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acdf892d0f23f1b59cdb0a32830ed1425cd20e29387afe28465e44528a5c4e5`  
		Last Modified: Thu, 31 Oct 2024 23:01:03 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:40` - linux; ppc64le

```console
$ docker pull fedora@sha256:5ef6eaf0e85cef827fddce7b92bc35513c76b17abf9c5e04d6560ab6d69757ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89389670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941bfff2032e29dccb779d934f2ad78f3b459b5f4f32447330bb2e8bcc15f609`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:31 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:31 GMT
ENV DISTTAG=f40container FGC=f40 FBR=f40
# Thu, 31 Oct 2024 11:44:31 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5b147ec9594da08f4b84877715ac6d0dc3e86936f67ae3715484a7eb784ad03e`  
		Last Modified: Thu, 31 Oct 2024 23:02:38 GMT  
		Size: 89.4 MB (89389670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:40` - unknown; unknown

```console
$ docker pull fedora@sha256:54884c4a5831b551037639a493760a45f7ca20fb09f41f279c32c0904dcee1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5107338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a7017efb712cd3a8c049093a286b77bb7c1254470662ecabe845f6e9b2de37`

```dockerfile
```

-	Layers:
	-	`sha256:5a3261d04336bfbb66e4fc6430e5025574032298898e4cbc9cc31eef68433410`  
		Size: 5.1 MB (5102333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4220f668d0665e2b7d34c74e727e23f1ebf70b24ac63e66feaaf1eb18b10d0b`  
		Size: 5.0 KB (5005 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:40` - linux; s390x

```console
$ docker pull fedora@sha256:295abb35664f3a2573010c0c8549b8f6c0514b63939572d835316f23227a6b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82948099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d886ee648d4543bcebdee394ce71f14bd20984316c6b8a8fc3db9ae8d9fbfbd8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:31 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:31 GMT
ENV DISTTAG=f40container FGC=f40 FBR=f40
# Thu, 31 Oct 2024 11:44:31 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:20d6560761db1eda9c24fe2030877e9e86c4209607b0734c63499d4cc916abf3`  
		Last Modified: Thu, 31 Oct 2024 23:02:21 GMT  
		Size: 82.9 MB (82948099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:40` - unknown; unknown

```console
$ docker pull fedora@sha256:c713ac7409c77076bc9e6e69b3b4732d9e6cd254ebf09ec584cfd23fe1a3e654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5108765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1212899664dd4a505ad34972e881784eb1448c0f76e6bb6d60dd44de019a3944`

```dockerfile
```

-	Layers:
	-	`sha256:6036a0378bb801b82f299a6a1ef054f5488e4a4bdfad0792ee35631ca8edda46`  
		Last Modified: Thu, 31 Oct 2024 23:02:19 GMT  
		Size: 5.1 MB (5103780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7802c66b647db2d8c1e1f0d44c9fbe433483e720322c2be79dcad8c9a66feaeb`  
		Last Modified: Thu, 31 Oct 2024 23:02:19 GMT  
		Size: 5.0 KB (4985 bytes)  
		MIME: application/vnd.in-toto+json

## `fedora:41`

```console
$ docker pull fedora@sha256:3ec60eb34fa1a095c0c34dd37cead9fd38afb62612d43892fcf1d3425c32bc1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fedora:41` - linux; amd64

```console
$ docker pull fedora@sha256:9cfb3a7ad0a36a1e943409def613ec495571a5683c45addb5d608c2c29bb8248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58596808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6787b90fe61e801687142277458584287469c9596c91766a43fa9f1e524c22`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:19 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:19 GMT
ENV DISTTAG=f41container FGC=f41 FBR=f41
# Thu, 31 Oct 2024 11:44:19 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c5a86865c5d3e78a4ab19ac7c516ffe93e41e0fd67f052a72f52d07cd2c59f9`  
		Last Modified: Thu, 31 Oct 2024 11:14:26 GMT  
		Size: 58.6 MB (58596808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:41` - unknown; unknown

```console
$ docker pull fedora@sha256:1a4c50024e4dbac78c462ac10aa9e65c99fc629f7f7364761f498d332157a01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2886157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fe45963c518c7dd38e677742aa9c30ab8ae841f94aebd302c7dc891ed3e11b`

```dockerfile
```

-	Layers:
	-	`sha256:6d25c887e287cf8c0e6cb6ae94da8721b6f3722f04e6fe1a38e29ac5f74f2252`  
		Last Modified: Thu, 31 Oct 2024 22:59:08 GMT  
		Size: 2.9 MB (2880871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed57bcc1ac9adaf0d9ed91f75014b074eaf95b694145130c4b92ae007fe2d438`  
		Last Modified: Thu, 31 Oct 2024 22:59:08 GMT  
		Size: 5.3 KB (5286 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:41` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:e77a6c0a222c3b9335cb637a16e70fa2133a4460382ef06d840b9880b812e8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57209276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e90bb0aca93fb835147280549f5b8047753f66b93076a4fa29f5173e7d289c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:19 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:19 GMT
ENV DISTTAG=f41container FGC=f41 FBR=f41
# Thu, 31 Oct 2024 11:44:19 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e3c408ecb0c25f0bcbefeb272d74ab9fba5836e7f68cc60cd46da7dc4ac7df03`  
		Last Modified: Thu, 31 Oct 2024 23:03:06 GMT  
		Size: 57.2 MB (57209276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:41` - unknown; unknown

```console
$ docker pull fedora@sha256:6b9427ba629dbe7a6e200528986b1afba982d98e4de4b9d6a49066e1b0013e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2886229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f915df99d1548bec83eb9626e2aad94414f4c3a043e33bec997764b02564620`

```dockerfile
```

-	Layers:
	-	`sha256:d221ca0874ef4fd4fa2476e8248fcfeb51f057f04b2c48d02edf07889df49cec`  
		Last Modified: Thu, 31 Oct 2024 23:03:04 GMT  
		Size: 2.9 MB (2880901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03e89972560ef4451e0f133b8fcf3934076b740ef001ba4dab2b988e2b4e29a3`  
		Last Modified: Thu, 31 Oct 2024 23:03:03 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:41` - linux; ppc64le

```console
$ docker pull fedora@sha256:c3f764afbd28eaac1732705b542c4cb5be7939e0ebeee341768039f9a8c27fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63928617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabe67b8aed6afae54f2638669f16037671222430cd1af6ed7c3aac47398858d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:19 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:19 GMT
ENV DISTTAG=f41container FGC=f41 FBR=f41
# Thu, 31 Oct 2024 11:44:19 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b38763202e3d51092c25e9400876e2521775bd406b970d030c98ed9f50ee45a2`  
		Last Modified: Thu, 31 Oct 2024 23:05:30 GMT  
		Size: 63.9 MB (63928617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:41` - unknown; unknown

```console
$ docker pull fedora@sha256:1d3dbcada8d311000003851d02489b631581e33f179ce797d736ba736940f6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2886829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905c8d2a12fa66eb6fc31978979c28ee11c7207538854a022c4cfc89e997e679`

```dockerfile
```

-	Layers:
	-	`sha256:f9a3465954b2e3e4dfb9506d86001112d244e44145e4278b9310a67eab752c9f`  
		Last Modified: Thu, 31 Oct 2024 23:05:28 GMT  
		Size: 2.9 MB (2881521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d84d77273c6c1649ddce19baa13930719155713f92282c344ba8ab5ee9d483c0`  
		Last Modified: Thu, 31 Oct 2024 23:05:28 GMT  
		Size: 5.3 KB (5308 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:41` - linux; s390x

```console
$ docker pull fedora@sha256:ec4b5e3901896d77beb495bef84779dd96fd91a4bc3efc9996ace2dc3c8ccaec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59426710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44b89c9b4b2c2c712f269203d6f9498ada25ab7e54674ca61285b5a5d0c2ab2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:19 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:19 GMT
ENV DISTTAG=f41container FGC=f41 FBR=f41
# Thu, 31 Oct 2024 11:44:19 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:46a98843a38519a1e191b4c7e885a6469c0649910463a7a57a7f15d0e1e51639`  
		Last Modified: Thu, 31 Oct 2024 23:04:37 GMT  
		Size: 59.4 MB (59426710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:41` - unknown; unknown

```console
$ docker pull fedora@sha256:d7b7a16e31bfbeec7f153d6c1d0dc1791e76b6d7ca5399205d418187e4deafd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2888659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a4b9e21621eae4f5d4d286f6993c3837b77968bb2b3e9996367c7ef7bb0497`

```dockerfile
```

-	Layers:
	-	`sha256:36d6aa3d5b0f058192cbfbea65372df4e653a2232397852245cd5d6cecf96fcf`  
		Last Modified: Thu, 31 Oct 2024 23:04:35 GMT  
		Size: 2.9 MB (2883376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3602b48792b0a53359576557420853a000efa4040f4adc4dd2fc9812efe7e14c`  
		Last Modified: Thu, 31 Oct 2024 23:04:35 GMT  
		Size: 5.3 KB (5283 bytes)  
		MIME: application/vnd.in-toto+json

## `fedora:42`

```console
$ docker pull fedora@sha256:70d5934128fe1b1abc97750dc358dad9cf499c11059f0ed720872fedcc4880d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fedora:42` - linux; amd64

```console
$ docker pull fedora@sha256:19fcecbd14f2c1e887cbeb974295f5fc0e7b81e2df133e4f1b47a6f65cd11737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57845665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d88bf74c998392280e13124cf35d2576cf903dcd5a6f69b1919b62ee9fd590`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:18 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:18 GMT
ENV DISTTAG=f42container FGC=f42 FBR=f42
# Thu, 31 Oct 2024 11:44:18 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dfdabcb2640443c0deaae9fd849c36fd5319d4d5ff7643cc69be869f4cd29a3d`  
		Last Modified: Thu, 31 Oct 2024 22:59:04 GMT  
		Size: 57.8 MB (57845665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:42` - unknown; unknown

```console
$ docker pull fedora@sha256:6f5e4b600590dfdc3dd9cca6fa9e582452729fa5c4d8b5cde49633e749a94f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2985462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c47c586b0e4e92dc58d0b831b870db813739abe62606c13c09676fb731c23ef`

```dockerfile
```

-	Layers:
	-	`sha256:d4cb8c572ce261f161fddfb5a35fbfa02da7e9e48f37a73ffdcb8db021192d80`  
		Last Modified: Thu, 31 Oct 2024 22:59:03 GMT  
		Size: 3.0 MB (2980174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1de2b429ab08aee560e6dbfd7e04d1451848db085d3faa7f45181e6c59dd907`  
		Last Modified: Thu, 31 Oct 2024 22:59:03 GMT  
		Size: 5.3 KB (5288 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:42` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:63a62239306df94a1a3bdd6b60acc926651d5b05bd98b6a2667e2a29fb6632fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57017542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f74a2ffe1ba07fa3758a37879ce4608f45a2241bc84db6cbb24d87f17ba2025`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:18 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:18 GMT
ENV DISTTAG=f42container FGC=f42 FBR=f42
# Thu, 31 Oct 2024 11:44:18 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6371c29100f54798ef3869db4ba5566ca9d22ab21fb86cd983e6e0f8e27d321d`  
		Last Modified: Thu, 31 Oct 2024 23:04:54 GMT  
		Size: 57.0 MB (57017542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:42` - unknown; unknown

```console
$ docker pull fedora@sha256:661218b8764fdc73a6f1733e5ad12d74aa450940c57d439e04306dc32b575347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2985534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b47f5e2ef1c1e33b60ce55fd1c35011f378b307134e2f2733c121b040c66ef`

```dockerfile
```

-	Layers:
	-	`sha256:f0f600a572f7efe7e58dd4aca5c4e4923820bec00a21b0ad9a8e2eed5ca7711d`  
		Last Modified: Thu, 31 Oct 2024 23:04:52 GMT  
		Size: 3.0 MB (2980204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f666eee26d773c3670182967468c1605e7ac52ba3969399a8bccb38113547e1`  
		Last Modified: Thu, 31 Oct 2024 23:04:52 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:42` - linux; ppc64le

```console
$ docker pull fedora@sha256:43160761e2709bdc7fe8130ebacf8eeb4ad4d197bfb90ff4a039edb86ce73f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63656656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6e0a6b8bdb9a923827a734fd7d2a880e00a0bee09674fb5bdca117aa132e61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:18 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:18 GMT
ENV DISTTAG=f42container FGC=f42 FBR=f42
# Thu, 31 Oct 2024 11:44:18 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:95958c9e498bde7d3140062edb5276026031ccf3bd561f424b95ef32f9830ae8`  
		Last Modified: Thu, 31 Oct 2024 23:09:31 GMT  
		Size: 63.7 MB (63656656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:42` - unknown; unknown

```console
$ docker pull fedora@sha256:a4ac2238a79b4771401cbbbda16616db7b9b2fd9ba333e15ccde95549338ab1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89627945a72a875d7e4dee83d073cbd2d1fbf986128d3ee5a3692b0b4df36251`

```dockerfile
```

-	Layers:
	-	`sha256:9458daeb02064beb06d45609ccd26e9e91e311250cb8665eeef016c8e59e5d11`  
		Last Modified: Thu, 31 Oct 2024 23:09:29 GMT  
		Size: 3.0 MB (2978734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f68fc28f571f7c413907b840a27514598e6f0ac32abf12dcbe24010078aafc75`  
		Last Modified: Thu, 31 Oct 2024 23:09:28 GMT  
		Size: 5.3 KB (5311 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:42` - linux; s390x

```console
$ docker pull fedora@sha256:45cd8db21cb2654ebcdcd60594ef069d1201ffc7d23c4cfc482452132710d332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58683759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fcb5f64652fc4c99705f04d21660685dd2f56c3f9329725547acf767b674bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:18 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:18 GMT
ENV DISTTAG=f42container FGC=f42 FBR=f42
# Thu, 31 Oct 2024 11:44:18 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b3a64d5d4832c266768eaeae8ef4a265460d7b5367c4c2b15123428acb80fa46`  
		Last Modified: Thu, 31 Oct 2024 23:06:41 GMT  
		Size: 58.7 MB (58683759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:42` - unknown; unknown

```console
$ docker pull fedora@sha256:fe7f6cc64cc1cbf28d5ef3fbb5b7e5d35e990efbfd8ab1a256d63b9ee989f87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2985873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e390166d22180df500243bfe9373c6999714c76ba50a3db53266db8c6e27d6f`

```dockerfile
```

-	Layers:
	-	`sha256:1a53239ecf3cf58c168163a0def04791a6256d0eeef73ad4a1b553c89bd9a343`  
		Last Modified: Thu, 31 Oct 2024 23:06:40 GMT  
		Size: 3.0 MB (2980589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c793162a40b207db97f03718805b10669df73673e0b9a77c40f1117d2b3b97d1`  
		Last Modified: Thu, 31 Oct 2024 23:06:40 GMT  
		Size: 5.3 KB (5284 bytes)  
		MIME: application/vnd.in-toto+json

## `fedora:latest`

```console
$ docker pull fedora@sha256:3ec60eb34fa1a095c0c34dd37cead9fd38afb62612d43892fcf1d3425c32bc1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fedora:latest` - linux; amd64

```console
$ docker pull fedora@sha256:9cfb3a7ad0a36a1e943409def613ec495571a5683c45addb5d608c2c29bb8248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58596808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6787b90fe61e801687142277458584287469c9596c91766a43fa9f1e524c22`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:19 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:19 GMT
ENV DISTTAG=f41container FGC=f41 FBR=f41
# Thu, 31 Oct 2024 11:44:19 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c5a86865c5d3e78a4ab19ac7c516ffe93e41e0fd67f052a72f52d07cd2c59f9`  
		Last Modified: Thu, 31 Oct 2024 11:14:26 GMT  
		Size: 58.6 MB (58596808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:latest` - unknown; unknown

```console
$ docker pull fedora@sha256:1a4c50024e4dbac78c462ac10aa9e65c99fc629f7f7364761f498d332157a01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2886157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fe45963c518c7dd38e677742aa9c30ab8ae841f94aebd302c7dc891ed3e11b`

```dockerfile
```

-	Layers:
	-	`sha256:6d25c887e287cf8c0e6cb6ae94da8721b6f3722f04e6fe1a38e29ac5f74f2252`  
		Last Modified: Thu, 31 Oct 2024 22:59:08 GMT  
		Size: 2.9 MB (2880871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed57bcc1ac9adaf0d9ed91f75014b074eaf95b694145130c4b92ae007fe2d438`  
		Last Modified: Thu, 31 Oct 2024 22:59:08 GMT  
		Size: 5.3 KB (5286 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:latest` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:e77a6c0a222c3b9335cb637a16e70fa2133a4460382ef06d840b9880b812e8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57209276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e90bb0aca93fb835147280549f5b8047753f66b93076a4fa29f5173e7d289c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:19 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:19 GMT
ENV DISTTAG=f41container FGC=f41 FBR=f41
# Thu, 31 Oct 2024 11:44:19 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e3c408ecb0c25f0bcbefeb272d74ab9fba5836e7f68cc60cd46da7dc4ac7df03`  
		Last Modified: Thu, 31 Oct 2024 23:03:06 GMT  
		Size: 57.2 MB (57209276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:latest` - unknown; unknown

```console
$ docker pull fedora@sha256:6b9427ba629dbe7a6e200528986b1afba982d98e4de4b9d6a49066e1b0013e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2886229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f915df99d1548bec83eb9626e2aad94414f4c3a043e33bec997764b02564620`

```dockerfile
```

-	Layers:
	-	`sha256:d221ca0874ef4fd4fa2476e8248fcfeb51f057f04b2c48d02edf07889df49cec`  
		Last Modified: Thu, 31 Oct 2024 23:03:04 GMT  
		Size: 2.9 MB (2880901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03e89972560ef4451e0f133b8fcf3934076b740ef001ba4dab2b988e2b4e29a3`  
		Last Modified: Thu, 31 Oct 2024 23:03:03 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:latest` - linux; ppc64le

```console
$ docker pull fedora@sha256:c3f764afbd28eaac1732705b542c4cb5be7939e0ebeee341768039f9a8c27fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63928617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabe67b8aed6afae54f2638669f16037671222430cd1af6ed7c3aac47398858d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:19 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:19 GMT
ENV DISTTAG=f41container FGC=f41 FBR=f41
# Thu, 31 Oct 2024 11:44:19 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b38763202e3d51092c25e9400876e2521775bd406b970d030c98ed9f50ee45a2`  
		Last Modified: Thu, 31 Oct 2024 23:05:30 GMT  
		Size: 63.9 MB (63928617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:latest` - unknown; unknown

```console
$ docker pull fedora@sha256:1d3dbcada8d311000003851d02489b631581e33f179ce797d736ba736940f6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2886829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905c8d2a12fa66eb6fc31978979c28ee11c7207538854a022c4cfc89e997e679`

```dockerfile
```

-	Layers:
	-	`sha256:f9a3465954b2e3e4dfb9506d86001112d244e44145e4278b9310a67eab752c9f`  
		Last Modified: Thu, 31 Oct 2024 23:05:28 GMT  
		Size: 2.9 MB (2881521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d84d77273c6c1649ddce19baa13930719155713f92282c344ba8ab5ee9d483c0`  
		Last Modified: Thu, 31 Oct 2024 23:05:28 GMT  
		Size: 5.3 KB (5308 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:latest` - linux; s390x

```console
$ docker pull fedora@sha256:ec4b5e3901896d77beb495bef84779dd96fd91a4bc3efc9996ace2dc3c8ccaec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59426710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44b89c9b4b2c2c712f269203d6f9498ada25ab7e54674ca61285b5a5d0c2ab2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:19 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:19 GMT
ENV DISTTAG=f41container FGC=f41 FBR=f41
# Thu, 31 Oct 2024 11:44:19 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:46a98843a38519a1e191b4c7e885a6469c0649910463a7a57a7f15d0e1e51639`  
		Last Modified: Thu, 31 Oct 2024 23:04:37 GMT  
		Size: 59.4 MB (59426710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:latest` - unknown; unknown

```console
$ docker pull fedora@sha256:d7b7a16e31bfbeec7f153d6c1d0dc1791e76b6d7ca5399205d418187e4deafd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2888659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a4b9e21621eae4f5d4d286f6993c3837b77968bb2b3e9996367c7ef7bb0497`

```dockerfile
```

-	Layers:
	-	`sha256:36d6aa3d5b0f058192cbfbea65372df4e653a2232397852245cd5d6cecf96fcf`  
		Last Modified: Thu, 31 Oct 2024 23:04:35 GMT  
		Size: 2.9 MB (2883376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3602b48792b0a53359576557420853a000efa4040f4adc4dd2fc9812efe7e14c`  
		Last Modified: Thu, 31 Oct 2024 23:04:35 GMT  
		Size: 5.3 KB (5283 bytes)  
		MIME: application/vnd.in-toto+json

## `fedora:rawhide`

```console
$ docker pull fedora@sha256:70d5934128fe1b1abc97750dc358dad9cf499c11059f0ed720872fedcc4880d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fedora:rawhide` - linux; amd64

```console
$ docker pull fedora@sha256:19fcecbd14f2c1e887cbeb974295f5fc0e7b81e2df133e4f1b47a6f65cd11737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57845665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d88bf74c998392280e13124cf35d2576cf903dcd5a6f69b1919b62ee9fd590`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:18 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:18 GMT
ENV DISTTAG=f42container FGC=f42 FBR=f42
# Thu, 31 Oct 2024 11:44:18 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dfdabcb2640443c0deaae9fd849c36fd5319d4d5ff7643cc69be869f4cd29a3d`  
		Last Modified: Thu, 31 Oct 2024 22:59:04 GMT  
		Size: 57.8 MB (57845665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:rawhide` - unknown; unknown

```console
$ docker pull fedora@sha256:6f5e4b600590dfdc3dd9cca6fa9e582452729fa5c4d8b5cde49633e749a94f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2985462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c47c586b0e4e92dc58d0b831b870db813739abe62606c13c09676fb731c23ef`

```dockerfile
```

-	Layers:
	-	`sha256:d4cb8c572ce261f161fddfb5a35fbfa02da7e9e48f37a73ffdcb8db021192d80`  
		Last Modified: Thu, 31 Oct 2024 22:59:03 GMT  
		Size: 3.0 MB (2980174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1de2b429ab08aee560e6dbfd7e04d1451848db085d3faa7f45181e6c59dd907`  
		Last Modified: Thu, 31 Oct 2024 22:59:03 GMT  
		Size: 5.3 KB (5288 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:rawhide` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:63a62239306df94a1a3bdd6b60acc926651d5b05bd98b6a2667e2a29fb6632fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57017542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f74a2ffe1ba07fa3758a37879ce4608f45a2241bc84db6cbb24d87f17ba2025`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:18 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:18 GMT
ENV DISTTAG=f42container FGC=f42 FBR=f42
# Thu, 31 Oct 2024 11:44:18 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6371c29100f54798ef3869db4ba5566ca9d22ab21fb86cd983e6e0f8e27d321d`  
		Last Modified: Thu, 31 Oct 2024 23:04:54 GMT  
		Size: 57.0 MB (57017542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:rawhide` - unknown; unknown

```console
$ docker pull fedora@sha256:661218b8764fdc73a6f1733e5ad12d74aa450940c57d439e04306dc32b575347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2985534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b47f5e2ef1c1e33b60ce55fd1c35011f378b307134e2f2733c121b040c66ef`

```dockerfile
```

-	Layers:
	-	`sha256:f0f600a572f7efe7e58dd4aca5c4e4923820bec00a21b0ad9a8e2eed5ca7711d`  
		Last Modified: Thu, 31 Oct 2024 23:04:52 GMT  
		Size: 3.0 MB (2980204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f666eee26d773c3670182967468c1605e7ac52ba3969399a8bccb38113547e1`  
		Last Modified: Thu, 31 Oct 2024 23:04:52 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:rawhide` - linux; ppc64le

```console
$ docker pull fedora@sha256:43160761e2709bdc7fe8130ebacf8eeb4ad4d197bfb90ff4a039edb86ce73f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63656656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6e0a6b8bdb9a923827a734fd7d2a880e00a0bee09674fb5bdca117aa132e61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:18 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:18 GMT
ENV DISTTAG=f42container FGC=f42 FBR=f42
# Thu, 31 Oct 2024 11:44:18 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:95958c9e498bde7d3140062edb5276026031ccf3bd561f424b95ef32f9830ae8`  
		Last Modified: Thu, 31 Oct 2024 23:09:31 GMT  
		Size: 63.7 MB (63656656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:rawhide` - unknown; unknown

```console
$ docker pull fedora@sha256:a4ac2238a79b4771401cbbbda16616db7b9b2fd9ba333e15ccde95549338ab1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89627945a72a875d7e4dee83d073cbd2d1fbf986128d3ee5a3692b0b4df36251`

```dockerfile
```

-	Layers:
	-	`sha256:9458daeb02064beb06d45609ccd26e9e91e311250cb8665eeef016c8e59e5d11`  
		Last Modified: Thu, 31 Oct 2024 23:09:29 GMT  
		Size: 3.0 MB (2978734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f68fc28f571f7c413907b840a27514598e6f0ac32abf12dcbe24010078aafc75`  
		Last Modified: Thu, 31 Oct 2024 23:09:28 GMT  
		Size: 5.3 KB (5311 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:rawhide` - linux; s390x

```console
$ docker pull fedora@sha256:45cd8db21cb2654ebcdcd60594ef069d1201ffc7d23c4cfc482452132710d332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58683759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fcb5f64652fc4c99705f04d21660685dd2f56c3f9329725547acf767b674bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2024 11:44:18 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 31 Oct 2024 11:44:18 GMT
ENV DISTTAG=f42container FGC=f42 FBR=f42
# Thu, 31 Oct 2024 11:44:18 GMT
ADD fedora-20241031.tar / # buildkit
# Thu, 31 Oct 2024 11:44:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b3a64d5d4832c266768eaeae8ef4a265460d7b5367c4c2b15123428acb80fa46`  
		Last Modified: Thu, 31 Oct 2024 23:06:41 GMT  
		Size: 58.7 MB (58683759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:rawhide` - unknown; unknown

```console
$ docker pull fedora@sha256:fe7f6cc64cc1cbf28d5ef3fbb5b7e5d35e990efbfd8ab1a256d63b9ee989f87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2985873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e390166d22180df500243bfe9373c6999714c76ba50a3db53266db8c6e27d6f`

```dockerfile
```

-	Layers:
	-	`sha256:1a53239ecf3cf58c168163a0def04791a6256d0eeef73ad4a1b553c89bd9a343`  
		Last Modified: Thu, 31 Oct 2024 23:06:40 GMT  
		Size: 3.0 MB (2980589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c793162a40b207db97f03718805b10669df73673e0b9a77c40f1117d2b3b97d1`  
		Last Modified: Thu, 31 Oct 2024 23:06:40 GMT  
		Size: 5.3 KB (5284 bytes)  
		MIME: application/vnd.in-toto+json
