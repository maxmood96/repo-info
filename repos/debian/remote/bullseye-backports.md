## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:ae36909156dd7af52fe529b2ad7f1fe3f852615bd839270676f29749edfab210
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
$ docker pull debian@sha256:78cffdd109954bd17dc8a8ef5d7aa3b219e1ed1a5fb74149be3f989bf41bee7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53747965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5efd4df11ae7615e0fe2081887c7a5494c66e1545843d77de9d44cbaa739e8fb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50050b072242fd9ae5abdd5f46e92aeed7e5b8daf5a16173b6ce4faf476a12ec`  
		Last Modified: Thu, 08 May 2025 20:30:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7543578471ca8f5d9983d381191cfd2fa09ff6ac43a4655c44f220f5e4d2dbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e1acc10fdd7a08417cb7b03dcb88540e87c5ab99620c866a2686fe9a6affd2`

```dockerfile
```

-	Layers:
	-	`sha256:6be3094aef7e7c5f6b8e6afa1a7b5901fef99acdeaf233a8d4687c09e159f4a0`  
		Last Modified: Mon, 28 Apr 2025 21:41:54 GMT  
		Size: 3.9 MB (3919484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a14bfcaf4325240897d379d9202d47910702d1931d83d2d4eeb3bd8388842792`  
		Last Modified: Mon, 28 Apr 2025 21:41:54 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:f335a93fe5cd1f09d695e02426141029d12c0a9e5f2307c130e81393f6c22638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49040272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13882a64c552b4d4b9c3f42397ad4f3f83f36363a5de7a8a9c3abddb81a07356`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:72fa46f1d669ee2de1ffbc36b654bfe8dd0aad49156f4143a5d9edd3a5c3d559`  
		Last Modified: Thu, 08 May 2025 17:18:11 GMT  
		Size: 49.0 MB (49040048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d591bb1c6570b4f834e6f1b1fc5115fcec6a93f60860d15671e7d7dd8e4b927`  
		Last Modified: Mon, 28 Apr 2025 21:42:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e33d5939334ffca994392d0446b18253c554460e1396be167f6188bce9e8520a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3926945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1522c97a506a32e2e492d3bacbd036002d24f7be112a73a6c4dfcd882bf3d0`

```dockerfile
```

-	Layers:
	-	`sha256:e485c964a546aa1661ef7f38ebe1cef87133eedabfad38ad4745ba8180e2a33a`  
		Last Modified: Mon, 28 Apr 2025 21:42:34 GMT  
		Size: 3.9 MB (3921046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fce1149b22862283a99050edbe88107a4b485704dbdab8be5916ee2fd63c5344`  
		Last Modified: Mon, 28 Apr 2025 21:42:34 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:96aa88d255fe87fea403e8f4b68ffd10732460cb212bcec9eadfa26884c97511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52246205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ef99de7918fc2725a3efd1f9e13034dd1b135e9edbacbfbbf693cef7cf13bc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Thu, 08 May 2025 17:08:39 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44759ce5c77173a22feac6de4c6958d40a19305d98e1de8ada8895f27e009434`  
		Last Modified: Thu, 08 May 2025 20:12:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:86b2dfc50438fb257c0ae122b091ac9519cfc46af1c9477adf9929613f4bf98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d05b0a966641bc41dff4fe69f51b64995c2d123194c8d0d3b969293e21fce9f`

```dockerfile
```

-	Layers:
	-	`sha256:5ed3147575e74c327bf56f298d6a071ae379fa0c8435aac05fee9f9469b49293`  
		Last Modified: Mon, 28 Apr 2025 21:41:38 GMT  
		Size: 3.9 MB (3919064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be31c9dbe5cfb9d04a0ccff3342b3c82a9d6922ee2507a3407829f3377e70900`  
		Last Modified: Mon, 28 Apr 2025 21:41:38 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:6fbef8813b6a8757c15f9b5b57ea14864c203d361a7c90ca862e714ac9b06aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54683328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d1467c86425ec8610567d31cae7f9fc6ed5a44b3349eb6330ae0dcec5a6d14`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Thu, 08 May 2025 17:55:44 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c17ad9f2796df47e53ba526325ede14037ab28dcca4a42f4f6cc9a41ec6a494`  
		Last Modified: Mon, 28 Apr 2025 21:42:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f19b6e8f6365339ec4d1acb22830229e55982d6d3455aab3cb71f9f3a0979f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d07b13b3b7d68a15cb896d4a0659f50a7ddc464c5cd7c2a727bcd8ceaa98250`

```dockerfile
```

-	Layers:
	-	`sha256:c601902d33e48f5ac9ba28a1bf06e715da0e37c8dcf43e8db52402261adc0ea9`  
		Last Modified: Mon, 28 Apr 2025 21:42:04 GMT  
		Size: 3.9 MB (3915991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:680d188631e32dc0fd4090eab108215d997b9152ba3691cf42beb366095e5e73`  
		Last Modified: Mon, 28 Apr 2025 21:42:04 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json
