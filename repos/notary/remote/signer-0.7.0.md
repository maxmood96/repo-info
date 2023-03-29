## `notary:signer-0.7.0`

```console
$ docker pull notary@sha256:43e05c6330725c5c2057d2c457ec61127494117a02bdfe28ae0410e814237e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:signer-0.7.0` - linux; amd64

```console
$ docker pull notary@sha256:b451451cfc3ff2b3ed3531b7c4ee1751f7274d62f10091c60b7c025bb444a5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7571286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887308089eeb82138f74e647c17f3113c6c846860ab8280d8c4834cfc04c1cac`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Mon, 27 Mar 2023 22:27:14 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 27 Mar 2023 22:27:14 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 27 Mar 2023 22:27:14 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 27 Mar 2023 22:27:14 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 27 Mar 2023 22:27:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 27 Mar 2023 22:27:14 GMT
WORKDIR /notary/signer
# Mon, 27 Mar 2023 22:27:14 GMT
COPY /notary-signer ./ # buildkit
# Mon, 27 Mar 2023 22:27:14 GMT
RUN ./notary-signer --version # buildkit
# Mon, 27 Mar 2023 22:27:14 GMT
COPY ./signer-config.json . # buildkit
# Mon, 27 Mar 2023 22:27:14 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 27 Mar 2023 22:27:14 GMT
USER notary
# Mon, 27 Mar 2023 22:27:14 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 27 Mar 2023 22:27:14 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a8bf9348133d1e770b90e9991d3f65c555075470962fb5e1321cf7201947a6`  
		Last Modified: Sat, 11 Feb 2023 10:16:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0208e6d213823747dbf355ecd6e4879b414b1413e219476f0ffa3791d92aade7`  
		Last Modified: Sat, 11 Feb 2023 10:16:33 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d493d618de9e17ee762f975de4a34705ba3727cf61f7f1d5da4ab435cc22cd4`  
		Last Modified: Tue, 28 Mar 2023 02:13:51 GMT  
		Size: 4.8 MB (4761356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059959817411cb7c66e43fb8940ec50234182382b07df6d1e952b1d75f7c5eed`  
		Last Modified: Tue, 28 Mar 2023 02:13:50 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc260edd320f683d64e76cec9d3a8051509e27162845814569757d9bb7d88ab`  
		Last Modified: Tue, 28 Mar 2023 02:13:50 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2538040a234cf39723ab70837a4b66031f38a7977d57af936e3b6c63fa72c5f1`  
		Last Modified: Tue, 28 Mar 2023 02:13:50 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:1b859eda30eea52686ca1e25104c8f6c54b7a110e709d1a4f318ea05c4fc28fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8544b97c1f8075ef86c3cd4f54f6e27fde1a0da79ab270f04d28b956cb23bb2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:48 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Mon, 13 Mar 2023 16:12:48 GMT
CMD ["/bin/sh"]
# Mon, 27 Mar 2023 22:54:37 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 27 Mar 2023 22:54:37 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 27 Mar 2023 22:54:37 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 27 Mar 2023 22:54:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 27 Mar 2023 22:54:37 GMT
WORKDIR /notary/signer
# Mon, 27 Mar 2023 22:54:37 GMT
COPY /notary-signer ./ # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
RUN ./notary-signer --version # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
COPY ./signer-config.json . # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
USER notary
# Mon, 27 Mar 2023 22:54:37 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 27 Mar 2023 22:54:37 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b05793ac14c68387ad3a34fa8d5d4136f040e8b820b1eee3595d30529d87e46`  
		Last Modified: Wed, 08 Mar 2023 00:17:02 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8867bd3aa695c936397740852a2a23245f7a8147431da0dea7ea79cb52c3fb7`  
		Last Modified: Wed, 08 Mar 2023 00:17:12 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46389c4cd7729b78c0a52df7daa142aedd2c1e21f6d97ff7ebd1a32b0936e54`  
		Last Modified: Tue, 28 Mar 2023 00:21:07 GMT  
		Size: 4.5 MB (4524262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7249b0975a56b424c7ef1643a7155c785f29e8785efa46c4d98c1db7be99ef`  
		Last Modified: Tue, 28 Mar 2023 00:21:06 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4071d49d37fd4ab8f37c67b5104e1db516290ac99a3c7776fdaa98b1a113af66`  
		Last Modified: Tue, 28 Mar 2023 00:21:06 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52c19763db6fc8e5bce84d899dd56c58e816226c24f2804400fba9ec85ec9a0`  
		Last Modified: Tue, 28 Mar 2023 00:21:06 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:3836e9404592d371aec8ed15b178c357d12cd0720ad37ba4d5bcc7dd5242123b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7101765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ed5f87ecca2905504962cbb00cb37c5f08f588bc7f1b341a7803fb77aa360d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Mon, 27 Mar 2023 22:45:31 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 27 Mar 2023 22:45:31 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 27 Mar 2023 22:45:31 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 27 Mar 2023 22:45:31 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 27 Mar 2023 22:45:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 27 Mar 2023 22:45:31 GMT
WORKDIR /notary/signer
# Mon, 27 Mar 2023 22:45:31 GMT
COPY /notary-signer ./ # buildkit
# Mon, 27 Mar 2023 22:45:31 GMT
RUN ./notary-signer --version # buildkit
# Mon, 27 Mar 2023 22:45:31 GMT
COPY ./signer-config.json . # buildkit
# Mon, 27 Mar 2023 22:45:31 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 27 Mar 2023 22:45:31 GMT
USER notary
# Mon, 27 Mar 2023 22:45:31 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 27 Mar 2023 22:45:31 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b9e3dceb52b5f1909f74e5761d8b0968630630d4c5d37134133ff1529d57ca`  
		Last Modified: Sat, 11 Feb 2023 02:02:10 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9044747e4fd585aae1a06ddae8513379f85e397343798bc36f0e5504eaa9863f`  
		Last Modified: Sat, 11 Feb 2023 02:02:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6904ef39a3d51dc67e4e3006c8869cee5cf65eb487eae5eaab8f920d629dc7`  
		Last Modified: Tue, 28 Mar 2023 02:21:55 GMT  
		Size: 4.4 MB (4390100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea25ee316d890b24e7e066f324ae43f8b8e7792629454ce13c21ea519200d69`  
		Last Modified: Tue, 28 Mar 2023 02:21:55 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf2df959f9c87f7aab2ba1b9085b6a45e4af76147feb0c77f8b112689b789c9`  
		Last Modified: Tue, 28 Mar 2023 02:21:55 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db95952b05a31953fdd3a571de03106a128420a5dc0806923a0c57373b0c4b6e`  
		Last Modified: Tue, 28 Mar 2023 02:21:55 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:a13fe571c3bacd059f81d9991bad6e853300223bed4d60a1f5db03a5a9d954cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9cf968026b3a4eea522e50c91aa3ccd8305a932dc0b1a4d0bc6b470271b286e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:29 GMT
ADD file:59ac1f8f33f9b9727892b7e45b33f54ef3c20d9d876c49d6a4c057641821d68f in / 
# Fri, 10 Feb 2023 21:24:29 GMT
CMD ["/bin/sh"]
# Mon, 27 Mar 2023 22:38:33 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 27 Mar 2023 22:38:33 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 27 Mar 2023 22:38:33 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 27 Mar 2023 22:38:33 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 27 Mar 2023 22:38:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 27 Mar 2023 22:38:33 GMT
WORKDIR /notary/signer
# Mon, 27 Mar 2023 22:38:33 GMT
COPY /notary-signer ./ # buildkit
# Mon, 27 Mar 2023 22:38:33 GMT
RUN ./notary-signer --version # buildkit
# Mon, 27 Mar 2023 22:38:33 GMT
COPY ./signer-config.json . # buildkit
# Mon, 27 Mar 2023 22:38:33 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 27 Mar 2023 22:38:33 GMT
USER notary
# Mon, 27 Mar 2023 22:38:33 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 27 Mar 2023 22:38:33 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:0987f51cd58a7d03bc7d6ff0a3a0a843c1a3fefcd41e3c8adc3999ddde7441e8`  
		Last Modified: Fri, 10 Feb 2023 21:25:30 GMT  
		Size: 2.8 MB (2810653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a5d52ee7c24d6c22b90002a097b005546a90c2cbe5b10f3899de1861e70fc9`  
		Last Modified: Fri, 24 Mar 2023 05:08:41 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1e0249dd7d40a91951fcfbd39ec505db60d377f210de9b76fc83e19028a1f6`  
		Last Modified: Fri, 24 Mar 2023 05:08:49 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b36830511627252a4ffa9d6371d5b0668c2934b4bbd0bfac39813640451313`  
		Last Modified: Tue, 28 Mar 2023 03:19:07 GMT  
		Size: 4.6 MB (4575874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53958708168e30131b7a5ecb9f1e41ce55aa89fec563cac7272a9dda21d9eeef`  
		Last Modified: Tue, 28 Mar 2023 03:19:06 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c05ed0e718505d254fca45fce56f0ef0ef3d1612f6c7dd383dd85113042eaff`  
		Last Modified: Tue, 28 Mar 2023 03:19:06 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b67a9e7f95e86490f4ed5c672909b7bca84862b20985cff69c0d57a1c430a8f`  
		Last Modified: Tue, 28 Mar 2023 03:19:06 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:4d2232090121bf9ac15b6795c48c5cb044ec491cbf2301b1935d12acdcb08108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7102923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d39a2949abbafdea0115a7a57686e7dd4916cbd982427a0554c3e1e6ed549b3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Mon, 27 Mar 2023 22:22:31 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 27 Mar 2023 22:22:31 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 27 Mar 2023 22:22:31 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 27 Mar 2023 22:22:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 27 Mar 2023 22:22:31 GMT
WORKDIR /notary/signer
# Mon, 27 Mar 2023 22:22:31 GMT
COPY /notary-signer ./ # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
RUN ./notary-signer --version # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
COPY ./signer-config.json . # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
USER notary
# Mon, 27 Mar 2023 22:22:31 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 27 Mar 2023 22:22:31 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674d271c42b70a8c82b552b2772787a6cac62d60cdc88c599bd983e06b4b1199`  
		Last Modified: Sat, 11 Feb 2023 09:33:10 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11d0b9967527e3e2fe9a387dd1b08ba83b7816d9e3863fb0f3e9c0a13f0225d`  
		Last Modified: Sat, 11 Feb 2023 09:33:20 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff45c2db506b53371307bdc344c0861a7dd46c067b7093b0e1438a9169763bf2`  
		Last Modified: Tue, 28 Mar 2023 02:19:41 GMT  
		Size: 4.3 MB (4296127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a7745a51f0bb73870d3c3e51184f9e8c17cb255c610686303d779d8e8ae5f3`  
		Last Modified: Tue, 28 Mar 2023 02:19:40 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e7280e5333b6db0e7a4bd1040d64cdd22f0ea2a0be0e5915f04527f9e919b8`  
		Last Modified: Tue, 28 Mar 2023 02:19:40 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ad4046a4cfcff2ef9ed79f2cf56658913e7388f6452b8e517515c073ce64d7`  
		Last Modified: Tue, 28 Mar 2023 02:19:40 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:823461cd01b0fd0259a46f88378f2ef26a524180f73e7f7c597ff1a4a0e7d9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da5c2782a47cd55a3bd7cdf3bc6e1bbbf51e781214faf08e95d216dd742e1b3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Wed, 29 Mar 2023 17:42:02 GMT
ADD file:6c3b2d8f192a3a12e6df8bc7130bbc723b1a39aa71809d23b15cf80bc5135096 in / 
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 17:42:02 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
EXPOSE map[4444/tcp:{}]
# Wed, 29 Mar 2023 17:42:02 GMT
EXPOSE map[7899/tcp:{}]
# Wed, 29 Mar 2023 17:42:02 GMT
ENV INSTALLDIR=/notary/signer
# Wed, 29 Mar 2023 17:42:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Wed, 29 Mar 2023 17:42:02 GMT
WORKDIR /notary/signer
# Wed, 29 Mar 2023 17:42:02 GMT
COPY /notary-signer ./ # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
RUN ./notary-signer --version # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
COPY ./signer-config.json . # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
USER notary
# Wed, 29 Mar 2023 17:42:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:95cbbfdf0c760cbcde91603c8eee15ec60d4aa5f874b4a538babcd2df1709174`  
		Last Modified: Wed, 29 Mar 2023 17:42:37 GMT  
		Size: 2.6 MB (2593389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2496bacdc3e38b8319b094c7cd682983189e795236b61f362a29c0e8e94ceb5`  
		Last Modified: Wed, 29 Mar 2023 19:02:13 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896ac2c8f346280fd047876860be1d522eae075adf2d30efb94fdc4359a6a466`  
		Last Modified: Wed, 29 Mar 2023 19:02:18 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6285fd241fb1dfa279dda67f86a82bba946327691def1fa78a39f4c89ada4cca`  
		Last Modified: Wed, 29 Mar 2023 19:02:19 GMT  
		Size: 4.6 MB (4605233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6782926d2ef6333a909143ebaefd4b7625218c9d51736220d706c18042e58514`  
		Last Modified: Wed, 29 Mar 2023 19:02:18 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a74ae17430841be98efe2e7d781cd1e06e782f63bc9e518418223c65faad36`  
		Last Modified: Wed, 29 Mar 2023 19:02:18 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5dc0e9da342d2163be0a01321aec83eebcd17421d2e45306b09d0b270874ee`  
		Last Modified: Wed, 29 Mar 2023 19:02:18 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
