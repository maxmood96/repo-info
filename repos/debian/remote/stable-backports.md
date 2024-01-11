## `debian:stable-backports`

```console
$ docker pull debian@sha256:98d1ebe722d2d8e918b6819b7ca557e3244ef84559c92533c9410ec5785a7f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:52912dc8ef062520548a81f8ad16d824bb167e19f6d15145ab4c80381366ee72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49561723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64428a94235b02ebc7c4baee6e93a2ff76323bf6a2651804c2c29882a9ded415`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:39:54 GMT
ADD file:047a30d75eb6094220d2ea803e9070abe9788630406157bd28a0d16f457d386a in / 
# Thu, 11 Jan 2024 02:39:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:39:58 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0300a06effd4e6778dc8b7e222d6a55030319e4877656ff8d7b29dc44889210a`  
		Last Modified: Thu, 11 Jan 2024 02:45:42 GMT  
		Size: 49.6 MB (49561502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db848ef0ed3f43832e69659454471b8b948b5915bead02895047ae1ed1d5b37`  
		Last Modified: Thu, 11 Jan 2024 02:45:50 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:eed886c01d992232d1d24e67b40b6544e1927e21307cc225236706eeb5ac38f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47319317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccae4bcd19d6a51b5b39592ddf8158631b480899d4c92fe87a3b74a71e417138`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:50:37 GMT
ADD file:0d20f653f4b358fafb43e2454be734ea749355a0d897c1fcb3aa6cc4e3c7a2fc in / 
# Thu, 11 Jan 2024 01:50:37 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 01:50:43 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:04b8081dd8e5812792cdd6d895c8e2e05c8fe9ede9537b89a561ad945235a649`  
		Last Modified: Thu, 11 Jan 2024 01:56:25 GMT  
		Size: 47.3 MB (47319093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d6d8340f3b607b4461bb2644a78a2046b274f4662426e1f560502fad20dca9`  
		Last Modified: Thu, 11 Jan 2024 01:56:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b39d50a62ab41917b6044af4f91f23528f61c438fab522cf9cfc6715325ad1ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45156908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4a4c269abe78636f13f8fe54f7e058891e2bbdeba460930a22acc010cdb03c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:44:45 GMT
ADD file:8b3d31c8a6280473383a57bb40d2ccf96a71f9cd3d8a1b5ce9fbb5006c3446b4 in / 
# Thu, 11 Jan 2024 02:44:46 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:44:50 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:be1802ea3b44c8a11ad4ef11d19c5b2ff35545caf3a6639f962c5d0c7ecb9b93`  
		Last Modified: Thu, 11 Jan 2024 02:52:16 GMT  
		Size: 45.2 MB (45156688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecda0ac8090dba880d6f56d364d706c8df0d99b204e3e188646c6ec0eff6ec04`  
		Last Modified: Thu, 11 Jan 2024 02:52:25 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:33c549cb5a40ccbae6fcb0f374c5956f419720ef12369a717e00df170cb05d67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49592431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c36f59a2ec39db7e97f324b14c38d3359c3dfee7438888f4debf789e84602e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:02 GMT
ADD file:ceb7235e364fab6b1ccdcbe59847a5e49c5e88a6942466a4a2e10057e6010734 in / 
# Thu, 11 Jan 2024 02:42:02 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:42:05 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:46f9ca8b80c8e639dc1530de69ae71dd6178bfeaf4014bc359be7957fe0ec157`  
		Last Modified: Thu, 11 Jan 2024 02:47:33 GMT  
		Size: 49.6 MB (49592207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d628d27c08a9e59bfae89f86f451a7a2289e012d2106bfad425fe205432d5d77`  
		Last Modified: Thu, 11 Jan 2024 02:47:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:c302a9129f3f3069cf2f80579f8181cdc10edb4edc6c14336858e354e960f571
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50582176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0152f4c145afcaa1854c76a6a8518c1cf97dc8f82133df35e00e94de91ee873c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:40 GMT
ADD file:b5a64cd14fdef4a74b2e4bd2a14e382230fd8028b1509b8181caf548159162c2 in / 
# Thu, 11 Jan 2024 02:40:41 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:40:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5ed4d620ccea9a82b288676aa18d6059657c874f608815d033d41b41e950d1c1`  
		Last Modified: Thu, 11 Jan 2024 02:47:33 GMT  
		Size: 50.6 MB (50581954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1da0a0a57c084733e0db60f40d255125218e6a7ff0eb2608e89def1e1a9f0d`  
		Last Modified: Thu, 11 Jan 2024 02:47:42 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:6fe93d4e5d339bd938d236790c84fd0e63ae86e70b009cf2db566871ba8d33ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49548870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce823c944cc0a9169045dc768cb8008cb1950b917520482a617292cfbbe11c18`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:15:53 GMT
ADD file:700550c6a19237385756735a472f16bb703895bf5b50308a1922ef2ae2b7548a in / 
# Thu, 11 Jan 2024 02:15:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:16:12 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4e7cc71bd10ec77a88bd393ed105d4ebabb8d53cbfb3fcf89a159f388fbc13b9`  
		Last Modified: Thu, 11 Jan 2024 02:27:34 GMT  
		Size: 49.5 MB (49548646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff333b8e77a9d268ed25ac485e063ae7cb29a4d30b86aeaef022cfb4773d550e`  
		Last Modified: Thu, 11 Jan 2024 02:27:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:7bfd96d066fd283c7c75e328d051f95ed32d3cd6b80b1735c5feefe5a792c1b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53557846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b50596897560f18c2a2db419e6eb836cce9a5d22f40db5d87d21247d56d87f0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:36:12 GMT
ADD file:6c469eb39d7e20ba0143fc45ec33e672b619b6797fb4f540794790730eb45b7d in / 
# Thu, 11 Jan 2024 02:36:15 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:36:20 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:350691915a3f298e33ca406a4eb3a9e0fe471e9bdbeefe419a3be3c01eaced05`  
		Last Modified: Thu, 11 Jan 2024 02:41:50 GMT  
		Size: 53.6 MB (53557623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7596441331ca8b503ab1fa474f2688ae4da5b9d6a1300e31f23957ce8d020e`  
		Last Modified: Thu, 11 Jan 2024 02:41:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:45ea6c87affac024c35bc4cf78a407e9522a37ada3a14d9865e6a737e713a848
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47918101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b916864bc0cdb11d74955432dc986a2bd1970bf42e2add0eca57b0786d533f39`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:47:09 GMT
ADD file:9832bce32dbe1ca264c48f3703ad021ab8d330ee06857671a8b71423782ebdb2 in / 
# Thu, 11 Jan 2024 01:47:14 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 01:47:22 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b2581710ecf284e94b19d591188b4bf9a45ebeeefec28cce12accc0c406fcb95`  
		Last Modified: Thu, 11 Jan 2024 01:52:18 GMT  
		Size: 47.9 MB (47917881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5d6024ba6b130b7dbd2b0be9d7033585091403792093d11483bc8f1fc5bd0b`  
		Last Modified: Thu, 11 Jan 2024 01:52:24 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
