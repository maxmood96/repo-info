## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:89957b04113c0a228c234ec2b163c89ad3eaeaaf4ca2cf29e513f539c12105a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7270588a2f1d44b6515784c67c8887f7ae83def17069edd48910f555d7eda296
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.0 MB (543036131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acec5c4453b5b9e508505dc7ed855169c8df9f295df44f0cb767a4fa5d8ee71`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Oct 2021 22:19:45 GMT
ADD file:7aef897e53c30ca977c42dd7692208abbd381b7d2e7e07a91d929f3f0ac4ea5c in / 
# Thu, 21 Oct 2021 22:19:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Oct 2021 22:20:07 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-e9fd3b1031f9a7540f8249e5d30e6439633e1eb09f394919e35ac5017ec18c93.tar.gz"  && echo "08179d9c712a9a7f501377be8ec5e1f7c229343a5bec655c93db62c623831c7c  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:5263c4cb36ce7acd05658a221ec502b376a281d7a6075ad09beb23ac02a7668c`  
		Last Modified: Wed, 20 Oct 2021 18:03:24 GMT  
		Size: 62.0 MB (61976108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9dd65b340056c10ece74bbe3f53f0a1ec019751a8d9b835573cac406fda501`  
		Last Modified: Thu, 21 Oct 2021 22:21:05 GMT  
		Size: 481.1 MB (481060023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:f430c04ebeb56b96104035a268952662f973de96c4643d53f5ffc56fb8e1e4fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.5 MB (485506862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0843a85e5d33304d882cf4a230dcc700a1e35540601466316552791924470a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Dec 2021 21:25:17 GMT
ADD file:1f2ecfca149ab81a0527241077c1b366afd95b6b7a1dd91bddfd6c40988ba994 in / 
# Thu, 02 Dec 2021 21:25:18 GMT
CMD ["/bin/bash"]
# Thu, 02 Dec 2021 21:25:41 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-faddacaa94ce45cab3ebd75298e985ccc4100e074eae55e6692f4139b7719f13.tar.gz"  && echo "821fcdbe479764a7bf796e4f23a04df2ad960dc88f93f9dfb4492deb77ec6522  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:74f9a6be36f3bc3bf6041c40376d548e3a8b720a0455674b19e9174a9e567078`  
		Last Modified: Thu, 02 Dec 2021 21:26:12 GMT  
		Size: 63.7 MB (63692547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d2f71867fbb5d9040a4eeaff7f0e49f8cbb45e0b4a563c6f2a7d151c4cd47c`  
		Last Modified: Thu, 02 Dec 2021 21:26:51 GMT  
		Size: 421.8 MB (421814315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
