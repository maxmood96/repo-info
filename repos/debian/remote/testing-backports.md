## `debian:testing-backports`

```console
$ docker pull debian@sha256:12ee698e89865e2ca05225bcff58f2c78ba07982bf18b4c8a5a4befdf2a95fb5
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:1a63eab6d22d17cb3825c05c3476081cd495774b720f309c65ba7ec22ee22070
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55457413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d2e0d561be7a2bc91bcbcbaeee1a0b01d65d5a8242ad09236304fbcb4779a3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:22:48 GMT
ADD file:61e992a8cfedc03feb12ae278ba2f7ab32f2845c5dea31869b10861104700c33 in / 
# Wed, 17 Nov 2021 02:22:48 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:22:51 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:99a9589829e41c216113b415d3c0c9233e7e6498d6291141cdf85cc3042e2b65`  
		Last Modified: Wed, 17 Nov 2021 02:29:54 GMT  
		Size: 55.5 MB (55457188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7315fa08c421422153de53a1bd153deb92fc69f0b8fb7c1eaef5e13c4acaad2c`  
		Last Modified: Wed, 17 Nov 2021 02:30:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:3fde94fd6dc2dced4b43b42df46d714af96cc8bdda648679a22bafea7cb0bcd5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52954137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09766e7d334ea3714b61eaf6c196d60e88073508cdc0064cb9319f12b79138fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:56:45 GMT
ADD file:0d14c17e0e69329fce9d7d1e61b89cf8e6c737db31e1335887a18f31372845e1 in / 
# Wed, 17 Nov 2021 02:56:47 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:56:59 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:39cfde2a5b94ace860c7e198b8278cb8182e1751cf8aea78a2142bd971fd4dc7`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 53.0 MB (52953912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db55d1b7540b067391595ca95e56799ce744139a66c3b46fe66619afa7006e48`  
		Last Modified: Wed, 17 Nov 2021 03:15:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e6c65237faddc55262028b030dafe111a6f7292720add98216df351ad6fd2063
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50589184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae19dc1738a34453d77f7c5f911344ef46fe28b96e7e88bb63d21cbdef189dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:06:01 GMT
ADD file:8534f2bd64383fee1357c8ed655d672d2fbef92507e2f11927991fbda800894c in / 
# Wed, 17 Nov 2021 02:06:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:06:14 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f099bc7a544c0fb4c5bd6b5b93da81e7b614c293d9032904d5b37dae9baefe43`  
		Last Modified: Wed, 17 Nov 2021 02:23:28 GMT  
		Size: 50.6 MB (50588959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5f34119a13d10b1574733baadd3a547946864926973228efe0c3cf5565655b`  
		Last Modified: Wed, 17 Nov 2021 02:23:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3ff5108bb89b7d0d2f533b47dcf8b7195d9c0e6505d100485a314d8e82cb395c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54464618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f3c7bc1d2e2852613a7c84fde94ead968a9aaef007d68ccbd44d0e77c99b51`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:c4d68bcae684e69a17ac01569a16c332bc925c4359383dbf3f27066f3abb295c in / 
# Wed, 17 Nov 2021 02:43:01 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:43:07 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3306c77e3ba6c6431765bbac6b0bbfb35079cfb5d567c3db405aad7687a02603`  
		Last Modified: Wed, 17 Nov 2021 02:52:02 GMT  
		Size: 54.5 MB (54464394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b268af8c50dfeb7aaf05c78db001badc1728730f4d7985c3eef1fe34ec8916`  
		Last Modified: Wed, 17 Nov 2021 02:52:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:f40babdcf3bc442fd57d17fbc2b04b64d1470cdf45c5d6360e04f969da7f8366
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56490897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0f239b7fee7a5411d5db505e8ff1435c80d2b25ce6c446643828f84dff48ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:51 GMT
ADD file:c80f770b5632d56b98b8316b44faa1f5b198563a6d15dff26def1a3ae7d54592 in / 
# Wed, 17 Nov 2021 02:42:51 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:42:57 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ba340dba45e23d2a978b05efb8e288ba9a536ab823eb597434206a625be512fd`  
		Last Modified: Wed, 17 Nov 2021 02:53:17 GMT  
		Size: 56.5 MB (56490673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87f1044d339656b2f1bd8d398f4242f0948cae74c923c34180332956462b643`  
		Last Modified: Wed, 17 Nov 2021 02:53:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:49230c7ceaebac2485f27a7af0049f799d64982a23531fe2313acd2981d1f113
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54085904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b5dbb3396cfbe4b0a8f55993b6abcfad4f3c3301548d99e5ddea45d64417fe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:14:05 GMT
ADD file:30e601ec2657da85de30169806cb5ef200f97a0d3d60df75dc47ca1630d05f2a in / 
# Wed, 17 Nov 2021 02:14:06 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:14:13 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:49bde980a154e1f7547c1e42d9a012d0d2660cce77784eb4997c24a35a6c5e2a`  
		Last Modified: Wed, 17 Nov 2021 02:25:08 GMT  
		Size: 54.1 MB (54085678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddef526b2c6697b20fb1afeda1bbd423a74484190b9f2ccd98eae795ec8987e`  
		Last Modified: Wed, 17 Nov 2021 02:25:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:9e3c39a2c4432137da727787e18ae428ea12f36dfdf4c813a5dcd56e47a5a333
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59706332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c838dc60d8eadbb19b20a5d831326dc22e973f055d3f56b223b76bee02ba532e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 03:35:47 GMT
ADD file:6ec33732a5ce54ae880804c7d4ce9bbc89ad76007b04d23e694d60679162abdc in / 
# Wed, 17 Nov 2021 03:36:09 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:37:20 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1c92bc8c2e6cbcb9f02ae352b98981f7632bf82483d2ab5a0394f4a3139b3c5b`  
		Last Modified: Wed, 17 Nov 2021 04:12:49 GMT  
		Size: 59.7 MB (59706108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef0f52d5c4aaa96e76420e8169c0b31d1d9afde93e1bf873f6dedf2e749994`  
		Last Modified: Wed, 17 Nov 2021 04:13:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:6027914093fc1280d22d7fd85f944020ee2ef5e501ca736305b88aa3c2ecc644
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53669412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e01388f51f58cd4a3bd79c8ae54a48df7add1b34ebc3161f5f1b2353e5d434`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:44:42 GMT
ADD file:6b07f3691aed718fdd31338ceb571ce22ffe4f9410f48df5c16f190258ace5ae in / 
# Wed, 17 Nov 2021 02:44:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:44:51 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1c02d7cb6bfcee3d40b1f3c9461f47e72e2f51d514b5df5ddb147d175da65910`  
		Last Modified: Wed, 17 Nov 2021 02:50:40 GMT  
		Size: 53.7 MB (53669187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1936d53cdd6ac9bc0483465e90743bf275dc82a32ddb19601dd4903c2cecba5a`  
		Last Modified: Wed, 17 Nov 2021 02:50:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
