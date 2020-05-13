## `debian:experimental-20200511`

```console
$ docker pull debian@sha256:da1a4b9cff5bffb5433ad923e2aa987e642d3bc8c03919ede6b3fa4a4ac1ade7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; s390x

### `debian:experimental-20200511` - linux; amd64

```console
$ docker pull debian@sha256:27f0fd86653b0bb3a2744bdfb909a3789d7ef137993733aed57a164b381a493f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51391170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba5400875a6a925fb672cc4c52f20bae7f6dcbc052efb7f0a537e120e19a91a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:24:45 GMT
ADD file:4a3ce6e28b74ce2c37d1a283b3b5a52d6754e078dfe7ce5a536dca9801dea0d2 in / 
# Wed, 13 May 2020 21:24:45 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:25:05 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:112696f5bff38e4ee46806902fa2be474354c1abaa6a6ba8f65a49d1aa97f812`  
		Last Modified: Wed, 13 May 2020 21:31:35 GMT  
		Size: 51.4 MB (51390951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f64a88466a51eb217fc60bfebc8e184b655df5479ec05d26295702ec4cc6563`  
		Last Modified: Wed, 13 May 2020 21:31:52 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20200511` - linux; arm variant v7

```console
$ docker pull debian@sha256:b1c65c45cbe51b8b6354fbd0aad9725611505cc2d6f02813a83968b5f174102f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47161419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53cbfbff0f9e3ae0cdb94d32acfdeed12acf15546300ec9f6a1515b701968389`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:20:44 GMT
ADD file:3b6b8dd9fe4a90210aefd064ff9295a0ccb81fa41e0e1884a187578c121ba607 in / 
# Wed, 13 May 2020 21:20:48 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:21:17 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c88ac45bee6ed1ce37ebbfce4905798f0f3dc239af61aeb27e4fb79c243e5e64`  
		Last Modified: Wed, 13 May 2020 21:29:51 GMT  
		Size: 47.2 MB (47161196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dced87d4c3d280f0e2575da5eab8f9f0da9ea332d66aa1815d141695351d7cf`  
		Last Modified: Wed, 13 May 2020 21:30:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20200511` - linux; s390x

```console
$ docker pull debian@sha256:65fb2dcf1d5d28c9f4c19e457738c1909a7d6f54650de2ea35aef815a4f72dc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50002226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd33fa862f3ae2e018ef69fe8c81178fb9ceb62444c75f63df6125db23ec8f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:45:22 GMT
ADD file:70201fe502819ff471e290f66527c1f6966d686e6cf5e15c34b34e91f9c371ad in / 
# Wed, 13 May 2020 21:45:24 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:45:43 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f783b35b669bd4b5a0dcf4a88f1f9f972f96a89ba4b6087493480a1a7cb1270f`  
		Last Modified: Wed, 13 May 2020 21:49:23 GMT  
		Size: 50.0 MB (50002005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e962ac1d72086fea1b66e0245f3ac5eb83aa212fbd41a5ebd4971dcf5c97bb2`  
		Last Modified: Wed, 13 May 2020 21:49:36 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
