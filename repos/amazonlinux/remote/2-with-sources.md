## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:88401a082ea5ed7c7f52bae11a93ac1b21e6be238e1e015c8d1125c81eb025ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:c09b199271ac2123d756575757bd922c47ce5a694f9db2918d60b8e091875875
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.2 MB (485180055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369eae5a9f20304404ae63efff50e98c2b4a2180a939d85b710cffcb8a1640c2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Jan 2022 02:20:04 GMT
ADD file:618cac8c5b6f6ff56ce221df12002d34997bcc996a0af3200b58db07d68be275 in / 
# Wed, 12 Jan 2022 02:20:04 GMT
CMD ["/bin/bash"]
# Wed, 12 Jan 2022 02:23:00 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-7aacabcecad2264904d2033d4072bf9e9b01b2723fb3de24f8df40bdfc2d34f7.tar.gz"  && echo "eba78093a05bb779050f6f4b93732638f4e1c21fb83c321416e0756efa88a089  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:3a461b3ae562f8b6cf015b4c480a21b630a874f7fec851457680159226c81632`  
		Last Modified: Mon, 10 Jan 2022 23:29:44 GMT  
		Size: 62.2 MB (62212074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f95733a61d793aea825bb1d8d9524d99118ee03b09038bff8da69f10cc6cd8`  
		Last Modified: Wed, 12 Jan 2022 02:24:10 GMT  
		Size: 423.0 MB (422967981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:ad5d2555741764f400b006e21873f1d966bef7a06905709b08d884ca5046dc82
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.8 MB (486804859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69dcd260e7799a7e5ad30046fd6a56a731b92f7603c7eadff3195f6a9f5ae419`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Jan 2022 02:39:41 GMT
ADD file:afc90ca87d61fdaef5c9d192a5151ab745ac8b8ea4d7544c2dfdd66bdb3b7993 in / 
# Wed, 12 Jan 2022 02:39:43 GMT
CMD ["/bin/bash"]
# Wed, 12 Jan 2022 02:41:20 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-7aacabcecad2264904d2033d4072bf9e9b01b2723fb3de24f8df40bdfc2d34f7.tar.gz"  && echo "eba78093a05bb779050f6f4b93732638f4e1c21fb83c321416e0756efa88a089  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:b2e274b2b0f90c3d6329566163244a0f2e6d97e4c010c62133388ac89652105f`  
		Last Modified: Wed, 12 Jan 2022 02:41:56 GMT  
		Size: 63.8 MB (63836908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f335cb87be6e36244e570c6194cee7b36f34f1af6d0f2c4a2c61430b67b7071`  
		Last Modified: Wed, 12 Jan 2022 02:42:43 GMT  
		Size: 423.0 MB (422967951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
