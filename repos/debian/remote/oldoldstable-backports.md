## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:5a50289e8ee46ceb3e5e627c8a86173ad966231321597cf2c09a9d7e7196c5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:1485490640111777c0f1998e3680b779ee50f566af86c8e54a7dd615a5eecbfe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50498222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c07cdd7c99fdbd5dfaa95156f4d640ab72b30d18756262ff4481caff2414db`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:40 GMT
ADD file:5904548c7cebe86d8cc57c026ace74b16641c827ffeda42b583579ab4eeadc10 in / 
# Thu, 27 Jul 2023 23:25:40 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:25:44 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:58ca768125d9edad02f86eabe3a91bb7f738e885db5f548309dc4032244629aa`  
		Last Modified: Thu, 27 Jul 2023 23:31:08 GMT  
		Size: 50.5 MB (50497992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dedff65ab1936132ab2c7898e06c60efeb85df4b6ebfcc4af9bf7e3a0e2ca2`  
		Last Modified: Thu, 27 Jul 2023 23:31:17 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e4782959639583bc3759c718c711d33e2aeeac01f2d475cb02606321047517b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45966434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd6f6d85e49b09554579c47808cde7a8aee3a08a80a1cb938a7adc1560b3632`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:58:58 GMT
ADD file:ff181fb8e7b3bfe42b3ecfde7d330ed92beb69bd17a23b6fb44d4d1099529d86 in / 
# Thu, 27 Jul 2023 23:58:59 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:59:03 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8a2da13915ac485da0fe0627bbe8d8287daf25ae815c9acf738ce1a100b8d019`  
		Last Modified: Fri, 28 Jul 2023 00:04:58 GMT  
		Size: 46.0 MB (45966204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f2b407fb1b91dfb229899ef8408fde06db4b45839c4a3be164a44cfd5a3fc4`  
		Last Modified: Fri, 28 Jul 2023 00:05:06 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:246c0794aacddeb6c3823881a15a05137b0222062e9a3c8a4b9f54db0f05c582
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49291094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130806215b142fa9e02ace9c2fa448129bd0a0f5a1fd8679c343f39d6ba0302f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:35 GMT
ADD file:f5e66bbf16b13c8688364cfea9d65a1be2ec403bc97acd59c9292527ce242b9d in / 
# Thu, 27 Jul 2023 23:43:36 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:43:38 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ecf46b8dac3fb3427e2a737955b5f48ab99c7d2c9d1d6531597ca10b95ad48dd`  
		Last Modified: Thu, 27 Jul 2023 23:48:07 GMT  
		Size: 49.3 MB (49290866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1f896a091e8f3b0b3037d47f9337a5a92bd85cba7a43e25a7567c6ce5d67a8`  
		Last Modified: Thu, 27 Jul 2023 23:48:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:f29e14579916cc9ad6fda6d1387e299d05cd739e217f29a5aa565a22c5dd21c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51255687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2feadf7e1c519cfd52cea9e62745cfd8df6d08b13aab8d4b1ba2dac86401532e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:48 GMT
ADD file:f4dfeb6ae81908c41b6fe6aa4eac1a3235c4bd03bd87e8a7f1c6680fc2f168c6 in / 
# Thu, 27 Jul 2023 23:39:49 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:39:51 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9e78655ab05c515d49db2078eef7f06c9fada609d50fa6b6b5e76ed3a344639e`  
		Last Modified: Thu, 27 Jul 2023 23:45:19 GMT  
		Size: 51.3 MB (51255458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c67c404b139f5bec1fd1b8223c699964691864fe2b5b7c32b10484b9be475f`  
		Last Modified: Thu, 27 Jul 2023 23:45:28 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
