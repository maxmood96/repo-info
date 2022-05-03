## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:80da29f4cf9bf60bc08b1beb080657856fc15cbd9592b54b323e629e24050d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:67fd44e1ca29a3c41ea875774083e64f218643232b1f5f27dfb1b1e4b6aeebf1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.7 MB (485656205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511c70976d4f4738c09199e01633142618f58f7bc2345948fa514aba7741d28e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Apr 2022 22:19:57 GMT
ADD file:4eb88d9d977dadb40c630d693a07ca066069b30b9751b7a421dfb4ba0b99d862 in / 
# Thu, 21 Apr 2022 22:19:58 GMT
CMD ["/bin/bash"]
# Thu, 21 Apr 2022 22:20:24 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-915f4823664b0d5efa5a9e17372f52c1e32718dcd0045d286495168c62f27bf6.tar.gz"  && echo "ddee5f71296afcb2dc85200f657f30688a3edb91a3e317592c02d9b387c62d5b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ac1397dc8419bf1767b60a5cc5849b7130406030581d4542e48965801c303a70`  
		Last Modified: Thu, 21 Apr 2022 22:08:36 GMT  
		Size: 62.3 MB (62265199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf04fc591da032b75c5a1e2f399e07e93a1b66b3bc75b07fe457ede25a29d9d`  
		Last Modified: Thu, 21 Apr 2022 22:21:31 GMT  
		Size: 423.4 MB (423391006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:124eb9a22c4bd8d59ea311f776bae5213d1e66db6103732c2c10741bb263f459
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.3 MB (487323598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671abfcb4f4c6d925fbecf84883a36ca87a0e7e8aa40bc10b0c3a1678f2b1168`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 May 2022 22:39:32 GMT
ADD file:c351a8c80719ef38e02c26849f50bb7d79c24a6347cc2a72ae1a0768964bd113 in / 
# Tue, 03 May 2022 22:39:34 GMT
CMD ["/bin/bash"]
# Tue, 03 May 2022 22:39:57 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-27e5885b1b2e681d27e9e8c451079b8f7f6444b820900db76e8e1f583d454a37.tar.gz"  && echo "fae8bd9cc002cf6ab3af9d777f1bc2646993e0340f2ffac4ddc984a5821a77c2  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ec3b4c26678b188d3874bed5e14dd278311fc05c81e418d5f0da36ec38d9f488`  
		Last Modified: Tue, 03 May 2022 03:07:52 GMT  
		Size: 63.9 MB (63902179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189fd58a2d5dc106fd8a0dee23c67eaa14f4c78c0e8fecb154e921df7a05540e`  
		Last Modified: Tue, 03 May 2022 22:41:23 GMT  
		Size: 423.4 MB (423421419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
