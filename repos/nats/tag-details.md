<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.21`](#nats2-alpine321)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.21`](#nats210-alpine321)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.25`](#nats21025)
-	[`nats:2.10.25-alpine`](#nats21025-alpine)
-	[`nats:2.10.25-alpine3.21`](#nats21025-alpine321)
-	[`nats:2.10.25-linux`](#nats21025-linux)
-	[`nats:2.10.25-nanoserver`](#nats21025-nanoserver)
-	[`nats:2.10.25-nanoserver-1809`](#nats21025-nanoserver-1809)
-	[`nats:2.10.25-scratch`](#nats21025-scratch)
-	[`nats:2.10.25-windowsservercore`](#nats21025-windowsservercore)
-	[`nats:2.10.25-windowsservercore-1809`](#nats21025-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.21`](#natsalpine321)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:1f72530645acb97d46973ffbe7b4beb6346b9c55f4a9d36b351e4c6dad753314
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.6775; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:5f9c390b45453cb55529ee7c0ea98f58c9eabbcce148e1fdef04cf8bb9074318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83db84e70fa4a83064757f6f48ae4cd12235da8b6444c70a176a84fff960a37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f2627f3e9adc28bf86cb08c7e382ad970ea899ddc8152bfb60fd5c1fe3d202`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:75e8038c8bbb0b5265cc9122a86bb065eee9d00f5800dae8c6355b8e0a9a745c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c246d72201ffc987cb7434edb7ec9f2b3df97136614b9a40e54756cdb416b72c`

```dockerfile
```

-	Layers:
	-	`sha256:8b34f8855c6dd3c2902d6e451796443e80889b7eb89b66b903756ed07929a167`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:e85e9da7f86adb238cc8a5f7cc45cb0cd87026da70fd44b01e444b8695880f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6e1c8c71ac7babb677e1219162820552049a771bfaf5537fa064fffa339ed7`

```dockerfile
```

-	Layers:
	-	`sha256:e8ae39b919b42a4500939423db63925e2755fca7d061faec83734c4dffc694bf`  
		Last Modified: Thu, 09 Jan 2025 08:57:17 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:81ef7161b07b53e04c4d6f06ff23a819d82edadee1b5114894b84b92bded720a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e573b7356a8dbfa6f0f90b6f1497f8ecba7f2fc930d117eed09b38931f15c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27233802c95930c2c97db1227b08ff00f5b72b607338899c46d31ab86b6bf0dd`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:ecb2bac646bde161319e5d013dd2f9791829f8b7b50df01ea5e10a3279ba3ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3ca0a483861718e290eb7d3e383d11990c2a42ec5980d5659a8df8b26c0671`

```dockerfile
```

-	Layers:
	-	`sha256:9d64b38b227893816e7fee501b8785831fc41177c7da344d2d2efadecdda7a67`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb1f744d45f1644e0a037f18b19e702a46d0eab0646a1e32774a97c1fcb57184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e47297c017006a49499c9dee7f2dd3ef999d9a17436c2c953cbe33bdf5d0c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a726266688ce6f73cf80ad50c512147100f877e50266515a99de500c91b25db3`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:fc4ce673ed5064130d176a89dee2e7643c1bb6407189e6501d3189497186bae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b78f424798237f9dd0e444af21a5fe68199f541753007f102cbd75b9385c2`

```dockerfile
```

-	Layers:
	-	`sha256:111318d590c0977b2a4d6c59b0dc324c853d994ee49032d86aaece1580c4b1c9`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:95f9e2bc23a9b1b10811b86ee1a18a15ee38f77cf56c8910c2a0959012da7e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515e09b78e41cc7926864d6b6e92edc26698a05dcce8dc8aa4a0a025b7c57814`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2024e9028623ac2d4facbfcc79793de84acf606af93e2a58405c55018f61c3`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:44fb1e13792ffab815d9a53fd588385fc17ff1ecc7c8dd52892c212637697274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf8cb760d0ae4538dac4f977b136585f9a3fdbceb692f4bb41893a480cc9782`

```dockerfile
```

-	Layers:
	-	`sha256:d43b7aaceeecac687ad894b912b854ec92c740f29ce3595a404c8b016a36ede2`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:d995fdee651d809102842ddd4f623725fef095e961cd5da9d75f009bcffc6162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31a3e7f0b7232ae529ffc2136b0d5f60df4998428df319d1deffa87afacffa3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b0d648957d541b8618bbb5ede323354ca5ffe9aeb3d1dbc9c352ea097e36a2`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:10560c276ecc00ccc189dd50847ef3dae9a4250913fe911c13361caa0418554d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f6cd92d566df26ed30bfd04e03565d263f2a08a426b5029f4b5b3373dc7fb0`

```dockerfile
```

-	Layers:
	-	`sha256:f9e945fabe7afbcc493bd9ab31004b72d72a266d574fe373fc060704bc2f94a1`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:5f5322bba05b71576e20f209c4b340bd995bdcc31a29a5e40f898e03cd2d591a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161299217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ed26b7d3e8ce4cc01b1be218c7301f56f4ed9c1cef651493d28a2a6204f2dd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 17:50:12 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 Jan 2025 17:50:17 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78be4d7c7554d3cc03be58653079e805ee14881716e7be4da21ed08dc92aecf`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a53c7b6ebfde3e19109bda127b7e6dd65afe79e4f181aff08978e4eeb4f5f35`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 6.0 MB (6025790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43d64cb96be0aa298d48a5812e2c3932f539ffb951d2c5b686e9d942b3ad671`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fff7bbd5ae2661700128fd04b604cfb063ecfefd7316d5f3f135990a00f5f52`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaab287c955c223fb7639ef1c45f7ee8e6cb71fc27b5392944fb1ee749e7aad`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d6ccb426c9a0f0d72f25a723f8c4cfa93a19577d1cb7d21fd99203d4720936`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:b93ef5ffb1f01168b119eaa7d5bd09d06ee4a92b4ca28ec3518b787ebb2549ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:d13ec5ce79a02e1be937820dd36db611e25bd0c08cd9947fa9a5d52a56bf91fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10009883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f82ef16e19c3b28fbf0f9721ceb28da9a34e77fb6f56fafad647123fdeaa12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1389e727b51dad1da0eee4dab424d30b3adc248945c6624b675ac28518cdcf73`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 6.4 MB (6367199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc4d59184023bde8f1163df4dba49dbab7d5ad807a967cb82cc4bdb27ff582`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932199a7e681f9e316441810f9f8a601d6b3024a5f618243b53bcecedcbd26`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a76b53321a9e54c4ae8ac76d4d55092f5344ab9c7a82fc6bf862bb5733d9ac4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a382496dbdb27ac2143007c60c1a2e728f1540254eb46f2b87b08276231356c9`

```dockerfile
```

-	Layers:
	-	`sha256:ce9696da8d1ea1fef5a70bdc0029fd24523875e259b6b3c5d2e29019f972488a`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ed9c796cd3ad56226504a37fdf8d723fb1f733050b8ee6893303fb8430c675b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dfdedee7614113bcdb4520d226d7309166368c268a647cacf4bf5645bd525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da649493a411bfb623f54e86f3b76b40dd7a4bfe42657e83db8d93b71f990f9b`  
		Last Modified: Thu, 23 Jan 2025 20:25:54 GMT  
		Size: 6.0 MB (6017858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb48584554a799af85ef81eb2c395c20e47c0017220a17ea51de65df8274ea`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729c51637a5e23f0df73c5b3934fcf12277ac1f7a7f5c23e554aa98ae0729db`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:97b50584b37c7b333558bd30709d127c88db6736672dcf9acf4358bf8a61e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7f1819c6cba2205ce0b28e6fa6af3c4ca4bfa55deb159eb096942283441b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b47e162ec2703a2ad9bbdef39f28e43c84bdefecd159d4732315024c2d64413`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b5868815b3f528c23a20af1e84c47dd8c3d71b081bec3f282a5080fe0b2123e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9101218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6bd4698025702dc40ccfd1bfa1437953fc9ade0d587ba4e4231ad24d8a7dd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a6b1d44a89dcbf597c9907146e0a51867b4ed4bd2bea7cc517bf93c45e2010`  
		Last Modified: Wed, 08 Jan 2025 18:45:03 GMT  
		Size: 6.0 MB (6003136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca5d46780ac7652092f710b97ba2b37a1c234b0a767343d2041c4bc38b73489`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef8f7a4172b027ce9f98a8732748ade622adb95a4020c38fe9130d0a1d520e1`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ae2683b2444ef44f3dd8ef3e9ea4b2c2cef75fbd2b37f0d12a9ea0948267ac91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6861a34069ee4798adba6258e40dbc34c7d0bbd9cf2df4be451f8bdc77ccda38`

```dockerfile
```

-	Layers:
	-	`sha256:ce68aa0da6eb69d64dcd0cec911721097b7e4db8c1008eb156ed39bb796dee34`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a4da0fc57cf9fbacac471da654b026b79c7f5889a976137434112694c8aa53c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9911663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a90da8fe97e67cfe8003aefeb5e4d496f3c3c2d62b32983346f3e9a71d0ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252a7fd157e5483b31440b7ab2b9dd8fecaa1443ba922c59cc5c0a31e662941`  
		Last Modified: Thu, 23 Jan 2025 20:25:57 GMT  
		Size: 5.9 MB (5918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c75f3d02cf31a351f067d9f29af8eb4e9d19d3cb202055c0d77f5e995a78e`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af341e5640fc20ff58015910ba702a5da4d8c4e86cf39cdd208e9f08e2c46cf8`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d15de15bf8ad9fa5e2d0819628e79168fb40d2ed9ad7d4446c8a3395e5d967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3223335912364a8d57333e693ef24420766757c49743b21adc40203d99a4bd0`

```dockerfile
```

-	Layers:
	-	`sha256:165668ceda68653b6dce0ef8330afde214a7cb42c094103ffd6a6e01835f7b64`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d5552c48e37011850332db8cc1693ec3e9a19234d16767b01bfb170e4c077c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f3e9720f21f14d69795e195215acb5783a4dcd0d766f47739b0251238825c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c646d1e663846cf15c587736bca653e994b2cc7dafa1c5915c0fafac7904392`  
		Last Modified: Thu, 23 Jan 2025 20:26:18 GMT  
		Size: 5.9 MB (5886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7e928a957a1d5442de03b0488186331a62f10c37fa16fa298a4abc86c737c`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddfc69be9741f053b51a5103d25dfaa6f95b62f104c5d3207dec92bfc5f519f`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cf7e706effbc29fca0c819608c4a0f8b3618cabab79f441d8ed0feee9f912e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf338df0b81a0519824480a6b8a7aa51d47848ac769911fa320be6392fad2e64`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf71bd8fdd1f5f4984f86346e93ea054c63b2107a413df819e4111b12b7d3b`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:a2d6f243fa355b743308898df4bedcec37e0ef296d72af3cdbebc87a700e7aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9680027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe977f5917123701c07307dbec905097239eef1be9974c4bf435a9716ebd2f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d56264cbb03f661c76ca48ea4695f8217d7897fc6ddbdbc6f74b5da4e61a620`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 6.2 MB (6212193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c252a87ccdd67c333282abcbcc17c60f67b9428fb3819dcbbad57724ffb313c8`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54677465f2d7d3ad44fe3e538dfab79e5ed4c76fede17650866a6d006c22d6`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:afcb335781617228f17afd454ce4d61c8e8c967ec19b1a648e00102c29a4345d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c7c47650157c85ba3e7f07706a129028c8e17bbd3fa6de2035359e35239b97`

```dockerfile
```

-	Layers:
	-	`sha256:b761dc077830ac087e4440bb5fa6c60ce2505d98fdd146865913031815e3c68f`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.21`

```console
$ docker pull nats@sha256:b93ef5ffb1f01168b119eaa7d5bd09d06ee4a92b4ca28ec3518b787ebb2549ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:d13ec5ce79a02e1be937820dd36db611e25bd0c08cd9947fa9a5d52a56bf91fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10009883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f82ef16e19c3b28fbf0f9721ceb28da9a34e77fb6f56fafad647123fdeaa12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1389e727b51dad1da0eee4dab424d30b3adc248945c6624b675ac28518cdcf73`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 6.4 MB (6367199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc4d59184023bde8f1163df4dba49dbab7d5ad807a967cb82cc4bdb27ff582`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932199a7e681f9e316441810f9f8a601d6b3024a5f618243b53bcecedcbd26`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:a76b53321a9e54c4ae8ac76d4d55092f5344ab9c7a82fc6bf862bb5733d9ac4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a382496dbdb27ac2143007c60c1a2e728f1540254eb46f2b87b08276231356c9`

```dockerfile
```

-	Layers:
	-	`sha256:ce9696da8d1ea1fef5a70bdc0029fd24523875e259b6b3c5d2e29019f972488a`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ed9c796cd3ad56226504a37fdf8d723fb1f733050b8ee6893303fb8430c675b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dfdedee7614113bcdb4520d226d7309166368c268a647cacf4bf5645bd525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da649493a411bfb623f54e86f3b76b40dd7a4bfe42657e83db8d93b71f990f9b`  
		Last Modified: Thu, 23 Jan 2025 20:25:54 GMT  
		Size: 6.0 MB (6017858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb48584554a799af85ef81eb2c395c20e47c0017220a17ea51de65df8274ea`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729c51637a5e23f0df73c5b3934fcf12277ac1f7a7f5c23e554aa98ae0729db`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:97b50584b37c7b333558bd30709d127c88db6736672dcf9acf4358bf8a61e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7f1819c6cba2205ce0b28e6fa6af3c4ca4bfa55deb159eb096942283441b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b47e162ec2703a2ad9bbdef39f28e43c84bdefecd159d4732315024c2d64413`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:b5868815b3f528c23a20af1e84c47dd8c3d71b081bec3f282a5080fe0b2123e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9101218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6bd4698025702dc40ccfd1bfa1437953fc9ade0d587ba4e4231ad24d8a7dd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a6b1d44a89dcbf597c9907146e0a51867b4ed4bd2bea7cc517bf93c45e2010`  
		Last Modified: Wed, 08 Jan 2025 18:45:03 GMT  
		Size: 6.0 MB (6003136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca5d46780ac7652092f710b97ba2b37a1c234b0a767343d2041c4bc38b73489`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef8f7a4172b027ce9f98a8732748ade622adb95a4020c38fe9130d0a1d520e1`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ae2683b2444ef44f3dd8ef3e9ea4b2c2cef75fbd2b37f0d12a9ea0948267ac91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6861a34069ee4798adba6258e40dbc34c7d0bbd9cf2df4be451f8bdc77ccda38`

```dockerfile
```

-	Layers:
	-	`sha256:ce68aa0da6eb69d64dcd0cec911721097b7e4db8c1008eb156ed39bb796dee34`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a4da0fc57cf9fbacac471da654b026b79c7f5889a976137434112694c8aa53c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9911663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a90da8fe97e67cfe8003aefeb5e4d496f3c3c2d62b32983346f3e9a71d0ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252a7fd157e5483b31440b7ab2b9dd8fecaa1443ba922c59cc5c0a31e662941`  
		Last Modified: Thu, 23 Jan 2025 20:25:57 GMT  
		Size: 5.9 MB (5918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c75f3d02cf31a351f067d9f29af8eb4e9d19d3cb202055c0d77f5e995a78e`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af341e5640fc20ff58015910ba702a5da4d8c4e86cf39cdd208e9f08e2c46cf8`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d15de15bf8ad9fa5e2d0819628e79168fb40d2ed9ad7d4446c8a3395e5d967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3223335912364a8d57333e693ef24420766757c49743b21adc40203d99a4bd0`

```dockerfile
```

-	Layers:
	-	`sha256:165668ceda68653b6dce0ef8330afde214a7cb42c094103ffd6a6e01835f7b64`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:d5552c48e37011850332db8cc1693ec3e9a19234d16767b01bfb170e4c077c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f3e9720f21f14d69795e195215acb5783a4dcd0d766f47739b0251238825c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c646d1e663846cf15c587736bca653e994b2cc7dafa1c5915c0fafac7904392`  
		Last Modified: Thu, 23 Jan 2025 20:26:18 GMT  
		Size: 5.9 MB (5886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7e928a957a1d5442de03b0488186331a62f10c37fa16fa298a4abc86c737c`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddfc69be9741f053b51a5103d25dfaa6f95b62f104c5d3207dec92bfc5f519f`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cf7e706effbc29fca0c819608c4a0f8b3618cabab79f441d8ed0feee9f912e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf338df0b81a0519824480a6b8a7aa51d47848ac769911fa320be6392fad2e64`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf71bd8fdd1f5f4984f86346e93ea054c63b2107a413df819e4111b12b7d3b`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:a2d6f243fa355b743308898df4bedcec37e0ef296d72af3cdbebc87a700e7aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9680027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe977f5917123701c07307dbec905097239eef1be9974c4bf435a9716ebd2f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d56264cbb03f661c76ca48ea4695f8217d7897fc6ddbdbc6f74b5da4e61a620`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 6.2 MB (6212193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c252a87ccdd67c333282abcbcc17c60f67b9428fb3819dcbbad57724ffb313c8`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54677465f2d7d3ad44fe3e538dfab79e5ed4c76fede17650866a6d006c22d6`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:afcb335781617228f17afd454ce4d61c8e8c967ec19b1a648e00102c29a4345d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c7c47650157c85ba3e7f07706a129028c8e17bbd3fa6de2035359e35239b97`

```dockerfile
```

-	Layers:
	-	`sha256:b761dc077830ac087e4440bb5fa6c60ce2505d98fdd146865913031815e3c68f`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:9e0236d18c30f44e0cbe71b1976e6465637af55d432cf87fd2dd04546ed19310
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:5f9c390b45453cb55529ee7c0ea98f58c9eabbcce148e1fdef04cf8bb9074318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83db84e70fa4a83064757f6f48ae4cd12235da8b6444c70a176a84fff960a37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f2627f3e9adc28bf86cb08c7e382ad970ea899ddc8152bfb60fd5c1fe3d202`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:75e8038c8bbb0b5265cc9122a86bb065eee9d00f5800dae8c6355b8e0a9a745c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c246d72201ffc987cb7434edb7ec9f2b3df97136614b9a40e54756cdb416b72c`

```dockerfile
```

-	Layers:
	-	`sha256:8b34f8855c6dd3c2902d6e451796443e80889b7eb89b66b903756ed07929a167`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e85e9da7f86adb238cc8a5f7cc45cb0cd87026da70fd44b01e444b8695880f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6e1c8c71ac7babb677e1219162820552049a771bfaf5537fa064fffa339ed7`

```dockerfile
```

-	Layers:
	-	`sha256:e8ae39b919b42a4500939423db63925e2755fca7d061faec83734c4dffc694bf`  
		Last Modified: Thu, 09 Jan 2025 08:57:17 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:81ef7161b07b53e04c4d6f06ff23a819d82edadee1b5114894b84b92bded720a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e573b7356a8dbfa6f0f90b6f1497f8ecba7f2fc930d117eed09b38931f15c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27233802c95930c2c97db1227b08ff00f5b72b607338899c46d31ab86b6bf0dd`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ecb2bac646bde161319e5d013dd2f9791829f8b7b50df01ea5e10a3279ba3ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3ca0a483861718e290eb7d3e383d11990c2a42ec5980d5659a8df8b26c0671`

```dockerfile
```

-	Layers:
	-	`sha256:9d64b38b227893816e7fee501b8785831fc41177c7da344d2d2efadecdda7a67`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb1f744d45f1644e0a037f18b19e702a46d0eab0646a1e32774a97c1fcb57184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e47297c017006a49499c9dee7f2dd3ef999d9a17436c2c953cbe33bdf5d0c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a726266688ce6f73cf80ad50c512147100f877e50266515a99de500c91b25db3`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:fc4ce673ed5064130d176a89dee2e7643c1bb6407189e6501d3189497186bae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b78f424798237f9dd0e444af21a5fe68199f541753007f102cbd75b9385c2`

```dockerfile
```

-	Layers:
	-	`sha256:111318d590c0977b2a4d6c59b0dc324c853d994ee49032d86aaece1580c4b1c9`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:95f9e2bc23a9b1b10811b86ee1a18a15ee38f77cf56c8910c2a0959012da7e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515e09b78e41cc7926864d6b6e92edc26698a05dcce8dc8aa4a0a025b7c57814`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2024e9028623ac2d4facbfcc79793de84acf606af93e2a58405c55018f61c3`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:44fb1e13792ffab815d9a53fd588385fc17ff1ecc7c8dd52892c212637697274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf8cb760d0ae4538dac4f977b136585f9a3fdbceb692f4bb41893a480cc9782`

```dockerfile
```

-	Layers:
	-	`sha256:d43b7aaceeecac687ad894b912b854ec92c740f29ce3595a404c8b016a36ede2`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:d995fdee651d809102842ddd4f623725fef095e961cd5da9d75f009bcffc6162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31a3e7f0b7232ae529ffc2136b0d5f60df4998428df319d1deffa87afacffa3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b0d648957d541b8618bbb5ede323354ca5ffe9aeb3d1dbc9c352ea097e36a2`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:10560c276ecc00ccc189dd50847ef3dae9a4250913fe911c13361caa0418554d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f6cd92d566df26ed30bfd04e03565d263f2a08a426b5029f4b5b3373dc7fb0`

```dockerfile
```

-	Layers:
	-	`sha256:f9e945fabe7afbcc493bd9ab31004b72d72a266d574fe373fc060704bc2f94a1`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:57c95a4019f74c260f06f9db81db80a8ee6251cc783f779429765a73bd7b4324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:5f5322bba05b71576e20f209c4b340bd995bdcc31a29a5e40f898e03cd2d591a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161299217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ed26b7d3e8ce4cc01b1be218c7301f56f4ed9c1cef651493d28a2a6204f2dd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 17:50:12 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 Jan 2025 17:50:17 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78be4d7c7554d3cc03be58653079e805ee14881716e7be4da21ed08dc92aecf`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a53c7b6ebfde3e19109bda127b7e6dd65afe79e4f181aff08978e4eeb4f5f35`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 6.0 MB (6025790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43d64cb96be0aa298d48a5812e2c3932f539ffb951d2c5b686e9d942b3ad671`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fff7bbd5ae2661700128fd04b604cfb063ecfefd7316d5f3f135990a00f5f52`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaab287c955c223fb7639ef1c45f7ee8e6cb71fc27b5392944fb1ee749e7aad`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d6ccb426c9a0f0d72f25a723f8c4cfa93a19577d1cb7d21fd99203d4720936`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:57c95a4019f74c260f06f9db81db80a8ee6251cc783f779429765a73bd7b4324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:5f5322bba05b71576e20f209c4b340bd995bdcc31a29a5e40f898e03cd2d591a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161299217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ed26b7d3e8ce4cc01b1be218c7301f56f4ed9c1cef651493d28a2a6204f2dd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 17:50:12 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 Jan 2025 17:50:17 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78be4d7c7554d3cc03be58653079e805ee14881716e7be4da21ed08dc92aecf`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a53c7b6ebfde3e19109bda127b7e6dd65afe79e4f181aff08978e4eeb4f5f35`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 6.0 MB (6025790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43d64cb96be0aa298d48a5812e2c3932f539ffb951d2c5b686e9d942b3ad671`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fff7bbd5ae2661700128fd04b604cfb063ecfefd7316d5f3f135990a00f5f52`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaab287c955c223fb7639ef1c45f7ee8e6cb71fc27b5392944fb1ee749e7aad`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d6ccb426c9a0f0d72f25a723f8c4cfa93a19577d1cb7d21fd99203d4720936`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:9e0236d18c30f44e0cbe71b1976e6465637af55d432cf87fd2dd04546ed19310
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:5f9c390b45453cb55529ee7c0ea98f58c9eabbcce148e1fdef04cf8bb9074318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83db84e70fa4a83064757f6f48ae4cd12235da8b6444c70a176a84fff960a37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f2627f3e9adc28bf86cb08c7e382ad970ea899ddc8152bfb60fd5c1fe3d202`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:75e8038c8bbb0b5265cc9122a86bb065eee9d00f5800dae8c6355b8e0a9a745c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c246d72201ffc987cb7434edb7ec9f2b3df97136614b9a40e54756cdb416b72c`

```dockerfile
```

-	Layers:
	-	`sha256:8b34f8855c6dd3c2902d6e451796443e80889b7eb89b66b903756ed07929a167`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e85e9da7f86adb238cc8a5f7cc45cb0cd87026da70fd44b01e444b8695880f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6e1c8c71ac7babb677e1219162820552049a771bfaf5537fa064fffa339ed7`

```dockerfile
```

-	Layers:
	-	`sha256:e8ae39b919b42a4500939423db63925e2755fca7d061faec83734c4dffc694bf`  
		Last Modified: Thu, 09 Jan 2025 08:57:17 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:81ef7161b07b53e04c4d6f06ff23a819d82edadee1b5114894b84b92bded720a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e573b7356a8dbfa6f0f90b6f1497f8ecba7f2fc930d117eed09b38931f15c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27233802c95930c2c97db1227b08ff00f5b72b607338899c46d31ab86b6bf0dd`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ecb2bac646bde161319e5d013dd2f9791829f8b7b50df01ea5e10a3279ba3ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3ca0a483861718e290eb7d3e383d11990c2a42ec5980d5659a8df8b26c0671`

```dockerfile
```

-	Layers:
	-	`sha256:9d64b38b227893816e7fee501b8785831fc41177c7da344d2d2efadecdda7a67`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb1f744d45f1644e0a037f18b19e702a46d0eab0646a1e32774a97c1fcb57184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e47297c017006a49499c9dee7f2dd3ef999d9a17436c2c953cbe33bdf5d0c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a726266688ce6f73cf80ad50c512147100f877e50266515a99de500c91b25db3`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:fc4ce673ed5064130d176a89dee2e7643c1bb6407189e6501d3189497186bae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b78f424798237f9dd0e444af21a5fe68199f541753007f102cbd75b9385c2`

```dockerfile
```

-	Layers:
	-	`sha256:111318d590c0977b2a4d6c59b0dc324c853d994ee49032d86aaece1580c4b1c9`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:95f9e2bc23a9b1b10811b86ee1a18a15ee38f77cf56c8910c2a0959012da7e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515e09b78e41cc7926864d6b6e92edc26698a05dcce8dc8aa4a0a025b7c57814`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2024e9028623ac2d4facbfcc79793de84acf606af93e2a58405c55018f61c3`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:44fb1e13792ffab815d9a53fd588385fc17ff1ecc7c8dd52892c212637697274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf8cb760d0ae4538dac4f977b136585f9a3fdbceb692f4bb41893a480cc9782`

```dockerfile
```

-	Layers:
	-	`sha256:d43b7aaceeecac687ad894b912b854ec92c740f29ce3595a404c8b016a36ede2`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:d995fdee651d809102842ddd4f623725fef095e961cd5da9d75f009bcffc6162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31a3e7f0b7232ae529ffc2136b0d5f60df4998428df319d1deffa87afacffa3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b0d648957d541b8618bbb5ede323354ca5ffe9aeb3d1dbc9c352ea097e36a2`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:10560c276ecc00ccc189dd50847ef3dae9a4250913fe911c13361caa0418554d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f6cd92d566df26ed30bfd04e03565d263f2a08a426b5029f4b5b3373dc7fb0`

```dockerfile
```

-	Layers:
	-	`sha256:f9e945fabe7afbcc493bd9ab31004b72d72a266d574fe373fc060704bc2f94a1`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:521666e383ff922ceb42fcda89d151092f909f6e1b07869e152e6fed707d9873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:4d0d68cf2f42b99731c82c9ae9fefde7da5d6603a050421c29f7f82e574dcc21
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128939081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71502b69ef80233acfce527fd9ee52d7af303fb5d8fbf153dacb04bab44baf26`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 20:26:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jan 2025 20:26:12 GMT
ENV NATS_DOCKERIZED=1
# Thu, 23 Jan 2025 20:26:12 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 20:26:13 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.25/nats-server-v2.10.25-windows-amd64.zip
# Thu, 23 Jan 2025 20:26:14 GMT
ENV NATS_SERVER_SHASUM=cfc706d1add1d61e7f00023f12ab8e4266f2dddce21ac1cb0934d261d793b185
# Thu, 23 Jan 2025 20:27:37 GMT
RUN Set-PSDebug -Trace 2
# Thu, 23 Jan 2025 20:28:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 23 Jan 2025 20:28:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 23 Jan 2025 20:28:06 GMT
EXPOSE 4222 6222 8222
# Thu, 23 Jan 2025 20:28:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 23 Jan 2025 20:28:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbeaae3c88fdde9250f605077db33243e114005915e5f8089d1fe52db9f7f33`  
		Last Modified: Thu, 23 Jan 2025 20:28:12 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7151274c33714e7509b14b4e0d5b0bb2edc7be2c5c6c367e23da47e5b0fe47e0`  
		Last Modified: Thu, 23 Jan 2025 20:28:12 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be62b080bac43f1250951e5538217700f365c04dbcffcab32948630b1fff874`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8c8166760128743ab6939afcc988275e618e512470c745110922e3c12ec02b`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccd23750ddffcb6549ccf53a46bdbe37f1638a006f0c386ebdef56518ded31c`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4289475cde28eda14db37afc21b3cd5e3e609b9a307fa2adc8e83e35aa5c939a`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 333.1 KB (333123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1770805cfbf8d0508a258a7289fb0322c417cd60a6ae7aba6c6d3e38a45c794`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 6.4 MB (6381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8342c5b961afa372660e90cd752e346589b10235666d4d67c897c2f4e8a7d671`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f571a3f111d510a76501240c7353c3e864c3833c64fc2df499c1351177d39f`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6db5f29326e04b49df5a4c674fd23399c971cece3510aacc7529cd4f1f60d34`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cc47ff9afa1bb9451e9405893d35ad5fed9e2bf17a54a03dca345b2b746bcd`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:521666e383ff922ceb42fcda89d151092f909f6e1b07869e152e6fed707d9873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:4d0d68cf2f42b99731c82c9ae9fefde7da5d6603a050421c29f7f82e574dcc21
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128939081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71502b69ef80233acfce527fd9ee52d7af303fb5d8fbf153dacb04bab44baf26`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 20:26:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jan 2025 20:26:12 GMT
ENV NATS_DOCKERIZED=1
# Thu, 23 Jan 2025 20:26:12 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 20:26:13 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.25/nats-server-v2.10.25-windows-amd64.zip
# Thu, 23 Jan 2025 20:26:14 GMT
ENV NATS_SERVER_SHASUM=cfc706d1add1d61e7f00023f12ab8e4266f2dddce21ac1cb0934d261d793b185
# Thu, 23 Jan 2025 20:27:37 GMT
RUN Set-PSDebug -Trace 2
# Thu, 23 Jan 2025 20:28:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 23 Jan 2025 20:28:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 23 Jan 2025 20:28:06 GMT
EXPOSE 4222 6222 8222
# Thu, 23 Jan 2025 20:28:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 23 Jan 2025 20:28:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbeaae3c88fdde9250f605077db33243e114005915e5f8089d1fe52db9f7f33`  
		Last Modified: Thu, 23 Jan 2025 20:28:12 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7151274c33714e7509b14b4e0d5b0bb2edc7be2c5c6c367e23da47e5b0fe47e0`  
		Last Modified: Thu, 23 Jan 2025 20:28:12 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be62b080bac43f1250951e5538217700f365c04dbcffcab32948630b1fff874`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8c8166760128743ab6939afcc988275e618e512470c745110922e3c12ec02b`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccd23750ddffcb6549ccf53a46bdbe37f1638a006f0c386ebdef56518ded31c`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4289475cde28eda14db37afc21b3cd5e3e609b9a307fa2adc8e83e35aa5c939a`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 333.1 KB (333123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1770805cfbf8d0508a258a7289fb0322c417cd60a6ae7aba6c6d3e38a45c794`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 6.4 MB (6381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8342c5b961afa372660e90cd752e346589b10235666d4d67c897c2f4e8a7d671`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f571a3f111d510a76501240c7353c3e864c3833c64fc2df499c1351177d39f`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6db5f29326e04b49df5a4c674fd23399c971cece3510aacc7529cd4f1f60d34`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cc47ff9afa1bb9451e9405893d35ad5fed9e2bf17a54a03dca345b2b746bcd`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:1f72530645acb97d46973ffbe7b4beb6346b9c55f4a9d36b351e4c6dad753314
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.6775; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:5f9c390b45453cb55529ee7c0ea98f58c9eabbcce148e1fdef04cf8bb9074318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83db84e70fa4a83064757f6f48ae4cd12235da8b6444c70a176a84fff960a37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f2627f3e9adc28bf86cb08c7e382ad970ea899ddc8152bfb60fd5c1fe3d202`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:75e8038c8bbb0b5265cc9122a86bb065eee9d00f5800dae8c6355b8e0a9a745c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c246d72201ffc987cb7434edb7ec9f2b3df97136614b9a40e54756cdb416b72c`

```dockerfile
```

-	Layers:
	-	`sha256:8b34f8855c6dd3c2902d6e451796443e80889b7eb89b66b903756ed07929a167`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:e85e9da7f86adb238cc8a5f7cc45cb0cd87026da70fd44b01e444b8695880f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6e1c8c71ac7babb677e1219162820552049a771bfaf5537fa064fffa339ed7`

```dockerfile
```

-	Layers:
	-	`sha256:e8ae39b919b42a4500939423db63925e2755fca7d061faec83734c4dffc694bf`  
		Last Modified: Thu, 09 Jan 2025 08:57:17 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:81ef7161b07b53e04c4d6f06ff23a819d82edadee1b5114894b84b92bded720a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e573b7356a8dbfa6f0f90b6f1497f8ecba7f2fc930d117eed09b38931f15c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27233802c95930c2c97db1227b08ff00f5b72b607338899c46d31ab86b6bf0dd`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:ecb2bac646bde161319e5d013dd2f9791829f8b7b50df01ea5e10a3279ba3ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3ca0a483861718e290eb7d3e383d11990c2a42ec5980d5659a8df8b26c0671`

```dockerfile
```

-	Layers:
	-	`sha256:9d64b38b227893816e7fee501b8785831fc41177c7da344d2d2efadecdda7a67`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb1f744d45f1644e0a037f18b19e702a46d0eab0646a1e32774a97c1fcb57184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e47297c017006a49499c9dee7f2dd3ef999d9a17436c2c953cbe33bdf5d0c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a726266688ce6f73cf80ad50c512147100f877e50266515a99de500c91b25db3`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:fc4ce673ed5064130d176a89dee2e7643c1bb6407189e6501d3189497186bae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b78f424798237f9dd0e444af21a5fe68199f541753007f102cbd75b9385c2`

```dockerfile
```

-	Layers:
	-	`sha256:111318d590c0977b2a4d6c59b0dc324c853d994ee49032d86aaece1580c4b1c9`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:95f9e2bc23a9b1b10811b86ee1a18a15ee38f77cf56c8910c2a0959012da7e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515e09b78e41cc7926864d6b6e92edc26698a05dcce8dc8aa4a0a025b7c57814`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2024e9028623ac2d4facbfcc79793de84acf606af93e2a58405c55018f61c3`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:44fb1e13792ffab815d9a53fd588385fc17ff1ecc7c8dd52892c212637697274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf8cb760d0ae4538dac4f977b136585f9a3fdbceb692f4bb41893a480cc9782`

```dockerfile
```

-	Layers:
	-	`sha256:d43b7aaceeecac687ad894b912b854ec92c740f29ce3595a404c8b016a36ede2`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:d995fdee651d809102842ddd4f623725fef095e961cd5da9d75f009bcffc6162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31a3e7f0b7232ae529ffc2136b0d5f60df4998428df319d1deffa87afacffa3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b0d648957d541b8618bbb5ede323354ca5ffe9aeb3d1dbc9c352ea097e36a2`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:10560c276ecc00ccc189dd50847ef3dae9a4250913fe911c13361caa0418554d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f6cd92d566df26ed30bfd04e03565d263f2a08a426b5029f4b5b3373dc7fb0`

```dockerfile
```

-	Layers:
	-	`sha256:f9e945fabe7afbcc493bd9ab31004b72d72a266d574fe373fc060704bc2f94a1`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:5f5322bba05b71576e20f209c4b340bd995bdcc31a29a5e40f898e03cd2d591a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161299217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ed26b7d3e8ce4cc01b1be218c7301f56f4ed9c1cef651493d28a2a6204f2dd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 17:50:12 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 Jan 2025 17:50:17 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78be4d7c7554d3cc03be58653079e805ee14881716e7be4da21ed08dc92aecf`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a53c7b6ebfde3e19109bda127b7e6dd65afe79e4f181aff08978e4eeb4f5f35`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 6.0 MB (6025790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43d64cb96be0aa298d48a5812e2c3932f539ffb951d2c5b686e9d942b3ad671`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fff7bbd5ae2661700128fd04b604cfb063ecfefd7316d5f3f135990a00f5f52`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaab287c955c223fb7639ef1c45f7ee8e6cb71fc27b5392944fb1ee749e7aad`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d6ccb426c9a0f0d72f25a723f8c4cfa93a19577d1cb7d21fd99203d4720936`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:b93ef5ffb1f01168b119eaa7d5bd09d06ee4a92b4ca28ec3518b787ebb2549ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:d13ec5ce79a02e1be937820dd36db611e25bd0c08cd9947fa9a5d52a56bf91fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10009883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f82ef16e19c3b28fbf0f9721ceb28da9a34e77fb6f56fafad647123fdeaa12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1389e727b51dad1da0eee4dab424d30b3adc248945c6624b675ac28518cdcf73`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 6.4 MB (6367199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc4d59184023bde8f1163df4dba49dbab7d5ad807a967cb82cc4bdb27ff582`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932199a7e681f9e316441810f9f8a601d6b3024a5f618243b53bcecedcbd26`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a76b53321a9e54c4ae8ac76d4d55092f5344ab9c7a82fc6bf862bb5733d9ac4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a382496dbdb27ac2143007c60c1a2e728f1540254eb46f2b87b08276231356c9`

```dockerfile
```

-	Layers:
	-	`sha256:ce9696da8d1ea1fef5a70bdc0029fd24523875e259b6b3c5d2e29019f972488a`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ed9c796cd3ad56226504a37fdf8d723fb1f733050b8ee6893303fb8430c675b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dfdedee7614113bcdb4520d226d7309166368c268a647cacf4bf5645bd525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da649493a411bfb623f54e86f3b76b40dd7a4bfe42657e83db8d93b71f990f9b`  
		Last Modified: Thu, 23 Jan 2025 20:25:54 GMT  
		Size: 6.0 MB (6017858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb48584554a799af85ef81eb2c395c20e47c0017220a17ea51de65df8274ea`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729c51637a5e23f0df73c5b3934fcf12277ac1f7a7f5c23e554aa98ae0729db`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:97b50584b37c7b333558bd30709d127c88db6736672dcf9acf4358bf8a61e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7f1819c6cba2205ce0b28e6fa6af3c4ca4bfa55deb159eb096942283441b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b47e162ec2703a2ad9bbdef39f28e43c84bdefecd159d4732315024c2d64413`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b5868815b3f528c23a20af1e84c47dd8c3d71b081bec3f282a5080fe0b2123e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9101218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6bd4698025702dc40ccfd1bfa1437953fc9ade0d587ba4e4231ad24d8a7dd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a6b1d44a89dcbf597c9907146e0a51867b4ed4bd2bea7cc517bf93c45e2010`  
		Last Modified: Wed, 08 Jan 2025 18:45:03 GMT  
		Size: 6.0 MB (6003136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca5d46780ac7652092f710b97ba2b37a1c234b0a767343d2041c4bc38b73489`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef8f7a4172b027ce9f98a8732748ade622adb95a4020c38fe9130d0a1d520e1`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ae2683b2444ef44f3dd8ef3e9ea4b2c2cef75fbd2b37f0d12a9ea0948267ac91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6861a34069ee4798adba6258e40dbc34c7d0bbd9cf2df4be451f8bdc77ccda38`

```dockerfile
```

-	Layers:
	-	`sha256:ce68aa0da6eb69d64dcd0cec911721097b7e4db8c1008eb156ed39bb796dee34`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a4da0fc57cf9fbacac471da654b026b79c7f5889a976137434112694c8aa53c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9911663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a90da8fe97e67cfe8003aefeb5e4d496f3c3c2d62b32983346f3e9a71d0ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252a7fd157e5483b31440b7ab2b9dd8fecaa1443ba922c59cc5c0a31e662941`  
		Last Modified: Thu, 23 Jan 2025 20:25:57 GMT  
		Size: 5.9 MB (5918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c75f3d02cf31a351f067d9f29af8eb4e9d19d3cb202055c0d77f5e995a78e`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af341e5640fc20ff58015910ba702a5da4d8c4e86cf39cdd208e9f08e2c46cf8`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d15de15bf8ad9fa5e2d0819628e79168fb40d2ed9ad7d4446c8a3395e5d967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3223335912364a8d57333e693ef24420766757c49743b21adc40203d99a4bd0`

```dockerfile
```

-	Layers:
	-	`sha256:165668ceda68653b6dce0ef8330afde214a7cb42c094103ffd6a6e01835f7b64`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d5552c48e37011850332db8cc1693ec3e9a19234d16767b01bfb170e4c077c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f3e9720f21f14d69795e195215acb5783a4dcd0d766f47739b0251238825c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c646d1e663846cf15c587736bca653e994b2cc7dafa1c5915c0fafac7904392`  
		Last Modified: Thu, 23 Jan 2025 20:26:18 GMT  
		Size: 5.9 MB (5886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7e928a957a1d5442de03b0488186331a62f10c37fa16fa298a4abc86c737c`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddfc69be9741f053b51a5103d25dfaa6f95b62f104c5d3207dec92bfc5f519f`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cf7e706effbc29fca0c819608c4a0f8b3618cabab79f441d8ed0feee9f912e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf338df0b81a0519824480a6b8a7aa51d47848ac769911fa320be6392fad2e64`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf71bd8fdd1f5f4984f86346e93ea054c63b2107a413df819e4111b12b7d3b`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:a2d6f243fa355b743308898df4bedcec37e0ef296d72af3cdbebc87a700e7aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9680027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe977f5917123701c07307dbec905097239eef1be9974c4bf435a9716ebd2f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d56264cbb03f661c76ca48ea4695f8217d7897fc6ddbdbc6f74b5da4e61a620`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 6.2 MB (6212193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c252a87ccdd67c333282abcbcc17c60f67b9428fb3819dcbbad57724ffb313c8`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54677465f2d7d3ad44fe3e538dfab79e5ed4c76fede17650866a6d006c22d6`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:afcb335781617228f17afd454ce4d61c8e8c967ec19b1a648e00102c29a4345d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c7c47650157c85ba3e7f07706a129028c8e17bbd3fa6de2035359e35239b97`

```dockerfile
```

-	Layers:
	-	`sha256:b761dc077830ac087e4440bb5fa6c60ce2505d98fdd146865913031815e3c68f`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.21`

```console
$ docker pull nats@sha256:b93ef5ffb1f01168b119eaa7d5bd09d06ee4a92b4ca28ec3518b787ebb2549ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:d13ec5ce79a02e1be937820dd36db611e25bd0c08cd9947fa9a5d52a56bf91fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10009883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f82ef16e19c3b28fbf0f9721ceb28da9a34e77fb6f56fafad647123fdeaa12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1389e727b51dad1da0eee4dab424d30b3adc248945c6624b675ac28518cdcf73`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 6.4 MB (6367199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc4d59184023bde8f1163df4dba49dbab7d5ad807a967cb82cc4bdb27ff582`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932199a7e681f9e316441810f9f8a601d6b3024a5f618243b53bcecedcbd26`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:a76b53321a9e54c4ae8ac76d4d55092f5344ab9c7a82fc6bf862bb5733d9ac4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a382496dbdb27ac2143007c60c1a2e728f1540254eb46f2b87b08276231356c9`

```dockerfile
```

-	Layers:
	-	`sha256:ce9696da8d1ea1fef5a70bdc0029fd24523875e259b6b3c5d2e29019f972488a`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ed9c796cd3ad56226504a37fdf8d723fb1f733050b8ee6893303fb8430c675b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dfdedee7614113bcdb4520d226d7309166368c268a647cacf4bf5645bd525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da649493a411bfb623f54e86f3b76b40dd7a4bfe42657e83db8d93b71f990f9b`  
		Last Modified: Thu, 23 Jan 2025 20:25:54 GMT  
		Size: 6.0 MB (6017858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb48584554a799af85ef81eb2c395c20e47c0017220a17ea51de65df8274ea`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729c51637a5e23f0df73c5b3934fcf12277ac1f7a7f5c23e554aa98ae0729db`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:97b50584b37c7b333558bd30709d127c88db6736672dcf9acf4358bf8a61e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7f1819c6cba2205ce0b28e6fa6af3c4ca4bfa55deb159eb096942283441b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b47e162ec2703a2ad9bbdef39f28e43c84bdefecd159d4732315024c2d64413`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:b5868815b3f528c23a20af1e84c47dd8c3d71b081bec3f282a5080fe0b2123e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9101218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6bd4698025702dc40ccfd1bfa1437953fc9ade0d587ba4e4231ad24d8a7dd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a6b1d44a89dcbf597c9907146e0a51867b4ed4bd2bea7cc517bf93c45e2010`  
		Last Modified: Wed, 08 Jan 2025 18:45:03 GMT  
		Size: 6.0 MB (6003136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca5d46780ac7652092f710b97ba2b37a1c234b0a767343d2041c4bc38b73489`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef8f7a4172b027ce9f98a8732748ade622adb95a4020c38fe9130d0a1d520e1`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ae2683b2444ef44f3dd8ef3e9ea4b2c2cef75fbd2b37f0d12a9ea0948267ac91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6861a34069ee4798adba6258e40dbc34c7d0bbd9cf2df4be451f8bdc77ccda38`

```dockerfile
```

-	Layers:
	-	`sha256:ce68aa0da6eb69d64dcd0cec911721097b7e4db8c1008eb156ed39bb796dee34`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a4da0fc57cf9fbacac471da654b026b79c7f5889a976137434112694c8aa53c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9911663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a90da8fe97e67cfe8003aefeb5e4d496f3c3c2d62b32983346f3e9a71d0ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252a7fd157e5483b31440b7ab2b9dd8fecaa1443ba922c59cc5c0a31e662941`  
		Last Modified: Thu, 23 Jan 2025 20:25:57 GMT  
		Size: 5.9 MB (5918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c75f3d02cf31a351f067d9f29af8eb4e9d19d3cb202055c0d77f5e995a78e`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af341e5640fc20ff58015910ba702a5da4d8c4e86cf39cdd208e9f08e2c46cf8`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d15de15bf8ad9fa5e2d0819628e79168fb40d2ed9ad7d4446c8a3395e5d967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3223335912364a8d57333e693ef24420766757c49743b21adc40203d99a4bd0`

```dockerfile
```

-	Layers:
	-	`sha256:165668ceda68653b6dce0ef8330afde214a7cb42c094103ffd6a6e01835f7b64`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:d5552c48e37011850332db8cc1693ec3e9a19234d16767b01bfb170e4c077c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f3e9720f21f14d69795e195215acb5783a4dcd0d766f47739b0251238825c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c646d1e663846cf15c587736bca653e994b2cc7dafa1c5915c0fafac7904392`  
		Last Modified: Thu, 23 Jan 2025 20:26:18 GMT  
		Size: 5.9 MB (5886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7e928a957a1d5442de03b0488186331a62f10c37fa16fa298a4abc86c737c`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddfc69be9741f053b51a5103d25dfaa6f95b62f104c5d3207dec92bfc5f519f`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cf7e706effbc29fca0c819608c4a0f8b3618cabab79f441d8ed0feee9f912e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf338df0b81a0519824480a6b8a7aa51d47848ac769911fa320be6392fad2e64`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf71bd8fdd1f5f4984f86346e93ea054c63b2107a413df819e4111b12b7d3b`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:a2d6f243fa355b743308898df4bedcec37e0ef296d72af3cdbebc87a700e7aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9680027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe977f5917123701c07307dbec905097239eef1be9974c4bf435a9716ebd2f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d56264cbb03f661c76ca48ea4695f8217d7897fc6ddbdbc6f74b5da4e61a620`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 6.2 MB (6212193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c252a87ccdd67c333282abcbcc17c60f67b9428fb3819dcbbad57724ffb313c8`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54677465f2d7d3ad44fe3e538dfab79e5ed4c76fede17650866a6d006c22d6`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:afcb335781617228f17afd454ce4d61c8e8c967ec19b1a648e00102c29a4345d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c7c47650157c85ba3e7f07706a129028c8e17bbd3fa6de2035359e35239b97`

```dockerfile
```

-	Layers:
	-	`sha256:b761dc077830ac087e4440bb5fa6c60ce2505d98fdd146865913031815e3c68f`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:9e0236d18c30f44e0cbe71b1976e6465637af55d432cf87fd2dd04546ed19310
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:5f9c390b45453cb55529ee7c0ea98f58c9eabbcce148e1fdef04cf8bb9074318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83db84e70fa4a83064757f6f48ae4cd12235da8b6444c70a176a84fff960a37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f2627f3e9adc28bf86cb08c7e382ad970ea899ddc8152bfb60fd5c1fe3d202`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:75e8038c8bbb0b5265cc9122a86bb065eee9d00f5800dae8c6355b8e0a9a745c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c246d72201ffc987cb7434edb7ec9f2b3df97136614b9a40e54756cdb416b72c`

```dockerfile
```

-	Layers:
	-	`sha256:8b34f8855c6dd3c2902d6e451796443e80889b7eb89b66b903756ed07929a167`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e85e9da7f86adb238cc8a5f7cc45cb0cd87026da70fd44b01e444b8695880f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6e1c8c71ac7babb677e1219162820552049a771bfaf5537fa064fffa339ed7`

```dockerfile
```

-	Layers:
	-	`sha256:e8ae39b919b42a4500939423db63925e2755fca7d061faec83734c4dffc694bf`  
		Last Modified: Thu, 09 Jan 2025 08:57:17 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:81ef7161b07b53e04c4d6f06ff23a819d82edadee1b5114894b84b92bded720a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e573b7356a8dbfa6f0f90b6f1497f8ecba7f2fc930d117eed09b38931f15c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27233802c95930c2c97db1227b08ff00f5b72b607338899c46d31ab86b6bf0dd`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ecb2bac646bde161319e5d013dd2f9791829f8b7b50df01ea5e10a3279ba3ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3ca0a483861718e290eb7d3e383d11990c2a42ec5980d5659a8df8b26c0671`

```dockerfile
```

-	Layers:
	-	`sha256:9d64b38b227893816e7fee501b8785831fc41177c7da344d2d2efadecdda7a67`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb1f744d45f1644e0a037f18b19e702a46d0eab0646a1e32774a97c1fcb57184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e47297c017006a49499c9dee7f2dd3ef999d9a17436c2c953cbe33bdf5d0c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a726266688ce6f73cf80ad50c512147100f877e50266515a99de500c91b25db3`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:fc4ce673ed5064130d176a89dee2e7643c1bb6407189e6501d3189497186bae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b78f424798237f9dd0e444af21a5fe68199f541753007f102cbd75b9385c2`

```dockerfile
```

-	Layers:
	-	`sha256:111318d590c0977b2a4d6c59b0dc324c853d994ee49032d86aaece1580c4b1c9`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:95f9e2bc23a9b1b10811b86ee1a18a15ee38f77cf56c8910c2a0959012da7e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515e09b78e41cc7926864d6b6e92edc26698a05dcce8dc8aa4a0a025b7c57814`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2024e9028623ac2d4facbfcc79793de84acf606af93e2a58405c55018f61c3`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:44fb1e13792ffab815d9a53fd588385fc17ff1ecc7c8dd52892c212637697274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf8cb760d0ae4538dac4f977b136585f9a3fdbceb692f4bb41893a480cc9782`

```dockerfile
```

-	Layers:
	-	`sha256:d43b7aaceeecac687ad894b912b854ec92c740f29ce3595a404c8b016a36ede2`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:d995fdee651d809102842ddd4f623725fef095e961cd5da9d75f009bcffc6162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31a3e7f0b7232ae529ffc2136b0d5f60df4998428df319d1deffa87afacffa3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b0d648957d541b8618bbb5ede323354ca5ffe9aeb3d1dbc9c352ea097e36a2`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:10560c276ecc00ccc189dd50847ef3dae9a4250913fe911c13361caa0418554d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f6cd92d566df26ed30bfd04e03565d263f2a08a426b5029f4b5b3373dc7fb0`

```dockerfile
```

-	Layers:
	-	`sha256:f9e945fabe7afbcc493bd9ab31004b72d72a266d574fe373fc060704bc2f94a1`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:57c95a4019f74c260f06f9db81db80a8ee6251cc783f779429765a73bd7b4324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:5f5322bba05b71576e20f209c4b340bd995bdcc31a29a5e40f898e03cd2d591a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161299217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ed26b7d3e8ce4cc01b1be218c7301f56f4ed9c1cef651493d28a2a6204f2dd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 17:50:12 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 Jan 2025 17:50:17 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78be4d7c7554d3cc03be58653079e805ee14881716e7be4da21ed08dc92aecf`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a53c7b6ebfde3e19109bda127b7e6dd65afe79e4f181aff08978e4eeb4f5f35`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 6.0 MB (6025790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43d64cb96be0aa298d48a5812e2c3932f539ffb951d2c5b686e9d942b3ad671`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fff7bbd5ae2661700128fd04b604cfb063ecfefd7316d5f3f135990a00f5f52`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaab287c955c223fb7639ef1c45f7ee8e6cb71fc27b5392944fb1ee749e7aad`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d6ccb426c9a0f0d72f25a723f8c4cfa93a19577d1cb7d21fd99203d4720936`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:57c95a4019f74c260f06f9db81db80a8ee6251cc783f779429765a73bd7b4324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:5f5322bba05b71576e20f209c4b340bd995bdcc31a29a5e40f898e03cd2d591a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161299217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ed26b7d3e8ce4cc01b1be218c7301f56f4ed9c1cef651493d28a2a6204f2dd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 17:50:12 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 Jan 2025 17:50:17 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78be4d7c7554d3cc03be58653079e805ee14881716e7be4da21ed08dc92aecf`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a53c7b6ebfde3e19109bda127b7e6dd65afe79e4f181aff08978e4eeb4f5f35`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 6.0 MB (6025790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43d64cb96be0aa298d48a5812e2c3932f539ffb951d2c5b686e9d942b3ad671`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fff7bbd5ae2661700128fd04b604cfb063ecfefd7316d5f3f135990a00f5f52`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaab287c955c223fb7639ef1c45f7ee8e6cb71fc27b5392944fb1ee749e7aad`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d6ccb426c9a0f0d72f25a723f8c4cfa93a19577d1cb7d21fd99203d4720936`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:9e0236d18c30f44e0cbe71b1976e6465637af55d432cf87fd2dd04546ed19310
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:5f9c390b45453cb55529ee7c0ea98f58c9eabbcce148e1fdef04cf8bb9074318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83db84e70fa4a83064757f6f48ae4cd12235da8b6444c70a176a84fff960a37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f2627f3e9adc28bf86cb08c7e382ad970ea899ddc8152bfb60fd5c1fe3d202`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:75e8038c8bbb0b5265cc9122a86bb065eee9d00f5800dae8c6355b8e0a9a745c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c246d72201ffc987cb7434edb7ec9f2b3df97136614b9a40e54756cdb416b72c`

```dockerfile
```

-	Layers:
	-	`sha256:8b34f8855c6dd3c2902d6e451796443e80889b7eb89b66b903756ed07929a167`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e85e9da7f86adb238cc8a5f7cc45cb0cd87026da70fd44b01e444b8695880f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6e1c8c71ac7babb677e1219162820552049a771bfaf5537fa064fffa339ed7`

```dockerfile
```

-	Layers:
	-	`sha256:e8ae39b919b42a4500939423db63925e2755fca7d061faec83734c4dffc694bf`  
		Last Modified: Thu, 09 Jan 2025 08:57:17 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:81ef7161b07b53e04c4d6f06ff23a819d82edadee1b5114894b84b92bded720a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e573b7356a8dbfa6f0f90b6f1497f8ecba7f2fc930d117eed09b38931f15c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27233802c95930c2c97db1227b08ff00f5b72b607338899c46d31ab86b6bf0dd`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ecb2bac646bde161319e5d013dd2f9791829f8b7b50df01ea5e10a3279ba3ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3ca0a483861718e290eb7d3e383d11990c2a42ec5980d5659a8df8b26c0671`

```dockerfile
```

-	Layers:
	-	`sha256:9d64b38b227893816e7fee501b8785831fc41177c7da344d2d2efadecdda7a67`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb1f744d45f1644e0a037f18b19e702a46d0eab0646a1e32774a97c1fcb57184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e47297c017006a49499c9dee7f2dd3ef999d9a17436c2c953cbe33bdf5d0c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a726266688ce6f73cf80ad50c512147100f877e50266515a99de500c91b25db3`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:fc4ce673ed5064130d176a89dee2e7643c1bb6407189e6501d3189497186bae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b78f424798237f9dd0e444af21a5fe68199f541753007f102cbd75b9385c2`

```dockerfile
```

-	Layers:
	-	`sha256:111318d590c0977b2a4d6c59b0dc324c853d994ee49032d86aaece1580c4b1c9`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:95f9e2bc23a9b1b10811b86ee1a18a15ee38f77cf56c8910c2a0959012da7e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515e09b78e41cc7926864d6b6e92edc26698a05dcce8dc8aa4a0a025b7c57814`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2024e9028623ac2d4facbfcc79793de84acf606af93e2a58405c55018f61c3`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:44fb1e13792ffab815d9a53fd588385fc17ff1ecc7c8dd52892c212637697274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf8cb760d0ae4538dac4f977b136585f9a3fdbceb692f4bb41893a480cc9782`

```dockerfile
```

-	Layers:
	-	`sha256:d43b7aaceeecac687ad894b912b854ec92c740f29ce3595a404c8b016a36ede2`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:d995fdee651d809102842ddd4f623725fef095e961cd5da9d75f009bcffc6162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31a3e7f0b7232ae529ffc2136b0d5f60df4998428df319d1deffa87afacffa3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b0d648957d541b8618bbb5ede323354ca5ffe9aeb3d1dbc9c352ea097e36a2`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:10560c276ecc00ccc189dd50847ef3dae9a4250913fe911c13361caa0418554d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f6cd92d566df26ed30bfd04e03565d263f2a08a426b5029f4b5b3373dc7fb0`

```dockerfile
```

-	Layers:
	-	`sha256:f9e945fabe7afbcc493bd9ab31004b72d72a266d574fe373fc060704bc2f94a1`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:521666e383ff922ceb42fcda89d151092f909f6e1b07869e152e6fed707d9873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:4d0d68cf2f42b99731c82c9ae9fefde7da5d6603a050421c29f7f82e574dcc21
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128939081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71502b69ef80233acfce527fd9ee52d7af303fb5d8fbf153dacb04bab44baf26`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 20:26:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jan 2025 20:26:12 GMT
ENV NATS_DOCKERIZED=1
# Thu, 23 Jan 2025 20:26:12 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 20:26:13 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.25/nats-server-v2.10.25-windows-amd64.zip
# Thu, 23 Jan 2025 20:26:14 GMT
ENV NATS_SERVER_SHASUM=cfc706d1add1d61e7f00023f12ab8e4266f2dddce21ac1cb0934d261d793b185
# Thu, 23 Jan 2025 20:27:37 GMT
RUN Set-PSDebug -Trace 2
# Thu, 23 Jan 2025 20:28:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 23 Jan 2025 20:28:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 23 Jan 2025 20:28:06 GMT
EXPOSE 4222 6222 8222
# Thu, 23 Jan 2025 20:28:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 23 Jan 2025 20:28:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbeaae3c88fdde9250f605077db33243e114005915e5f8089d1fe52db9f7f33`  
		Last Modified: Thu, 23 Jan 2025 20:28:12 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7151274c33714e7509b14b4e0d5b0bb2edc7be2c5c6c367e23da47e5b0fe47e0`  
		Last Modified: Thu, 23 Jan 2025 20:28:12 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be62b080bac43f1250951e5538217700f365c04dbcffcab32948630b1fff874`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8c8166760128743ab6939afcc988275e618e512470c745110922e3c12ec02b`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccd23750ddffcb6549ccf53a46bdbe37f1638a006f0c386ebdef56518ded31c`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4289475cde28eda14db37afc21b3cd5e3e609b9a307fa2adc8e83e35aa5c939a`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 333.1 KB (333123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1770805cfbf8d0508a258a7289fb0322c417cd60a6ae7aba6c6d3e38a45c794`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 6.4 MB (6381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8342c5b961afa372660e90cd752e346589b10235666d4d67c897c2f4e8a7d671`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f571a3f111d510a76501240c7353c3e864c3833c64fc2df499c1351177d39f`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6db5f29326e04b49df5a4c674fd23399c971cece3510aacc7529cd4f1f60d34`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cc47ff9afa1bb9451e9405893d35ad5fed9e2bf17a54a03dca345b2b746bcd`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:521666e383ff922ceb42fcda89d151092f909f6e1b07869e152e6fed707d9873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:4d0d68cf2f42b99731c82c9ae9fefde7da5d6603a050421c29f7f82e574dcc21
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128939081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71502b69ef80233acfce527fd9ee52d7af303fb5d8fbf153dacb04bab44baf26`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 20:26:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jan 2025 20:26:12 GMT
ENV NATS_DOCKERIZED=1
# Thu, 23 Jan 2025 20:26:12 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 20:26:13 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.25/nats-server-v2.10.25-windows-amd64.zip
# Thu, 23 Jan 2025 20:26:14 GMT
ENV NATS_SERVER_SHASUM=cfc706d1add1d61e7f00023f12ab8e4266f2dddce21ac1cb0934d261d793b185
# Thu, 23 Jan 2025 20:27:37 GMT
RUN Set-PSDebug -Trace 2
# Thu, 23 Jan 2025 20:28:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 23 Jan 2025 20:28:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 23 Jan 2025 20:28:06 GMT
EXPOSE 4222 6222 8222
# Thu, 23 Jan 2025 20:28:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 23 Jan 2025 20:28:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbeaae3c88fdde9250f605077db33243e114005915e5f8089d1fe52db9f7f33`  
		Last Modified: Thu, 23 Jan 2025 20:28:12 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7151274c33714e7509b14b4e0d5b0bb2edc7be2c5c6c367e23da47e5b0fe47e0`  
		Last Modified: Thu, 23 Jan 2025 20:28:12 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be62b080bac43f1250951e5538217700f365c04dbcffcab32948630b1fff874`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8c8166760128743ab6939afcc988275e618e512470c745110922e3c12ec02b`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccd23750ddffcb6549ccf53a46bdbe37f1638a006f0c386ebdef56518ded31c`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4289475cde28eda14db37afc21b3cd5e3e609b9a307fa2adc8e83e35aa5c939a`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 333.1 KB (333123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1770805cfbf8d0508a258a7289fb0322c417cd60a6ae7aba6c6d3e38a45c794`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 6.4 MB (6381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8342c5b961afa372660e90cd752e346589b10235666d4d67c897c2f4e8a7d671`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f571a3f111d510a76501240c7353c3e864c3833c64fc2df499c1351177d39f`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6db5f29326e04b49df5a4c674fd23399c971cece3510aacc7529cd4f1f60d34`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cc47ff9afa1bb9451e9405893d35ad5fed9e2bf17a54a03dca345b2b746bcd`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.25`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.10.25-alpine`

```console
$ docker pull nats@sha256:ceedb3202b699f0aeceb4dcd2bd26d7279fb2ff3d457e5c0f47f88eb5404be0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `nats:2.10.25-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ed9c796cd3ad56226504a37fdf8d723fb1f733050b8ee6893303fb8430c675b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dfdedee7614113bcdb4520d226d7309166368c268a647cacf4bf5645bd525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da649493a411bfb623f54e86f3b76b40dd7a4bfe42657e83db8d93b71f990f9b`  
		Last Modified: Thu, 23 Jan 2025 20:25:54 GMT  
		Size: 6.0 MB (6017858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb48584554a799af85ef81eb2c395c20e47c0017220a17ea51de65df8274ea`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729c51637a5e23f0df73c5b3934fcf12277ac1f7a7f5c23e554aa98ae0729db`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:97b50584b37c7b333558bd30709d127c88db6736672dcf9acf4358bf8a61e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7f1819c6cba2205ce0b28e6fa6af3c4ca4bfa55deb159eb096942283441b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b47e162ec2703a2ad9bbdef39f28e43c84bdefecd159d4732315024c2d64413`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a4da0fc57cf9fbacac471da654b026b79c7f5889a976137434112694c8aa53c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9911663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a90da8fe97e67cfe8003aefeb5e4d496f3c3c2d62b32983346f3e9a71d0ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252a7fd157e5483b31440b7ab2b9dd8fecaa1443ba922c59cc5c0a31e662941`  
		Last Modified: Thu, 23 Jan 2025 20:25:57 GMT  
		Size: 5.9 MB (5918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c75f3d02cf31a351f067d9f29af8eb4e9d19d3cb202055c0d77f5e995a78e`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af341e5640fc20ff58015910ba702a5da4d8c4e86cf39cdd208e9f08e2c46cf8`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d15de15bf8ad9fa5e2d0819628e79168fb40d2ed9ad7d4446c8a3395e5d967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3223335912364a8d57333e693ef24420766757c49743b21adc40203d99a4bd0`

```dockerfile
```

-	Layers:
	-	`sha256:165668ceda68653b6dce0ef8330afde214a7cb42c094103ffd6a6e01835f7b64`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d5552c48e37011850332db8cc1693ec3e9a19234d16767b01bfb170e4c077c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f3e9720f21f14d69795e195215acb5783a4dcd0d766f47739b0251238825c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c646d1e663846cf15c587736bca653e994b2cc7dafa1c5915c0fafac7904392`  
		Last Modified: Thu, 23 Jan 2025 20:26:18 GMT  
		Size: 5.9 MB (5886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7e928a957a1d5442de03b0488186331a62f10c37fa16fa298a4abc86c737c`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddfc69be9741f053b51a5103d25dfaa6f95b62f104c5d3207dec92bfc5f519f`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cf7e706effbc29fca0c819608c4a0f8b3618cabab79f441d8ed0feee9f912e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf338df0b81a0519824480a6b8a7aa51d47848ac769911fa320be6392fad2e64`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf71bd8fdd1f5f4984f86346e93ea054c63b2107a413df819e4111b12b7d3b`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.25-alpine3.21`

```console
$ docker pull nats@sha256:ceedb3202b699f0aeceb4dcd2bd26d7279fb2ff3d457e5c0f47f88eb5404be0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `nats:2.10.25-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ed9c796cd3ad56226504a37fdf8d723fb1f733050b8ee6893303fb8430c675b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dfdedee7614113bcdb4520d226d7309166368c268a647cacf4bf5645bd525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da649493a411bfb623f54e86f3b76b40dd7a4bfe42657e83db8d93b71f990f9b`  
		Last Modified: Thu, 23 Jan 2025 20:25:54 GMT  
		Size: 6.0 MB (6017858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb48584554a799af85ef81eb2c395c20e47c0017220a17ea51de65df8274ea`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729c51637a5e23f0df73c5b3934fcf12277ac1f7a7f5c23e554aa98ae0729db`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:97b50584b37c7b333558bd30709d127c88db6736672dcf9acf4358bf8a61e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7f1819c6cba2205ce0b28e6fa6af3c4ca4bfa55deb159eb096942283441b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b47e162ec2703a2ad9bbdef39f28e43c84bdefecd159d4732315024c2d64413`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a4da0fc57cf9fbacac471da654b026b79c7f5889a976137434112694c8aa53c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9911663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a90da8fe97e67cfe8003aefeb5e4d496f3c3c2d62b32983346f3e9a71d0ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252a7fd157e5483b31440b7ab2b9dd8fecaa1443ba922c59cc5c0a31e662941`  
		Last Modified: Thu, 23 Jan 2025 20:25:57 GMT  
		Size: 5.9 MB (5918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c75f3d02cf31a351f067d9f29af8eb4e9d19d3cb202055c0d77f5e995a78e`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af341e5640fc20ff58015910ba702a5da4d8c4e86cf39cdd208e9f08e2c46cf8`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d15de15bf8ad9fa5e2d0819628e79168fb40d2ed9ad7d4446c8a3395e5d967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3223335912364a8d57333e693ef24420766757c49743b21adc40203d99a4bd0`

```dockerfile
```

-	Layers:
	-	`sha256:165668ceda68653b6dce0ef8330afde214a7cb42c094103ffd6a6e01835f7b64`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.25-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:d5552c48e37011850332db8cc1693ec3e9a19234d16767b01bfb170e4c077c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f3e9720f21f14d69795e195215acb5783a4dcd0d766f47739b0251238825c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c646d1e663846cf15c587736bca653e994b2cc7dafa1c5915c0fafac7904392`  
		Last Modified: Thu, 23 Jan 2025 20:26:18 GMT  
		Size: 5.9 MB (5886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7e928a957a1d5442de03b0488186331a62f10c37fa16fa298a4abc86c737c`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddfc69be9741f053b51a5103d25dfaa6f95b62f104c5d3207dec92bfc5f519f`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.25-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cf7e706effbc29fca0c819608c4a0f8b3618cabab79f441d8ed0feee9f912e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf338df0b81a0519824480a6b8a7aa51d47848ac769911fa320be6392fad2e64`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf71bd8fdd1f5f4984f86346e93ea054c63b2107a413df819e4111b12b7d3b`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.25-linux`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.10.25-nanoserver`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.10.25-nanoserver-1809`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.10.25-scratch`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.10.25-windowsservercore`

```console
$ docker pull nats@sha256:521666e383ff922ceb42fcda89d151092f909f6e1b07869e152e6fed707d9873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `nats:2.10.25-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:4d0d68cf2f42b99731c82c9ae9fefde7da5d6603a050421c29f7f82e574dcc21
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128939081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71502b69ef80233acfce527fd9ee52d7af303fb5d8fbf153dacb04bab44baf26`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 20:26:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jan 2025 20:26:12 GMT
ENV NATS_DOCKERIZED=1
# Thu, 23 Jan 2025 20:26:12 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 20:26:13 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.25/nats-server-v2.10.25-windows-amd64.zip
# Thu, 23 Jan 2025 20:26:14 GMT
ENV NATS_SERVER_SHASUM=cfc706d1add1d61e7f00023f12ab8e4266f2dddce21ac1cb0934d261d793b185
# Thu, 23 Jan 2025 20:27:37 GMT
RUN Set-PSDebug -Trace 2
# Thu, 23 Jan 2025 20:28:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 23 Jan 2025 20:28:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 23 Jan 2025 20:28:06 GMT
EXPOSE 4222 6222 8222
# Thu, 23 Jan 2025 20:28:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 23 Jan 2025 20:28:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbeaae3c88fdde9250f605077db33243e114005915e5f8089d1fe52db9f7f33`  
		Last Modified: Thu, 23 Jan 2025 20:28:12 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7151274c33714e7509b14b4e0d5b0bb2edc7be2c5c6c367e23da47e5b0fe47e0`  
		Last Modified: Thu, 23 Jan 2025 20:28:12 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be62b080bac43f1250951e5538217700f365c04dbcffcab32948630b1fff874`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8c8166760128743ab6939afcc988275e618e512470c745110922e3c12ec02b`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccd23750ddffcb6549ccf53a46bdbe37f1638a006f0c386ebdef56518ded31c`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4289475cde28eda14db37afc21b3cd5e3e609b9a307fa2adc8e83e35aa5c939a`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 333.1 KB (333123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1770805cfbf8d0508a258a7289fb0322c417cd60a6ae7aba6c6d3e38a45c794`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 6.4 MB (6381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8342c5b961afa372660e90cd752e346589b10235666d4d67c897c2f4e8a7d671`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f571a3f111d510a76501240c7353c3e864c3833c64fc2df499c1351177d39f`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6db5f29326e04b49df5a4c674fd23399c971cece3510aacc7529cd4f1f60d34`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cc47ff9afa1bb9451e9405893d35ad5fed9e2bf17a54a03dca345b2b746bcd`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.25-windowsservercore-1809`

```console
$ docker pull nats@sha256:521666e383ff922ceb42fcda89d151092f909f6e1b07869e152e6fed707d9873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `nats:2.10.25-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:4d0d68cf2f42b99731c82c9ae9fefde7da5d6603a050421c29f7f82e574dcc21
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128939081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71502b69ef80233acfce527fd9ee52d7af303fb5d8fbf153dacb04bab44baf26`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 20:26:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jan 2025 20:26:12 GMT
ENV NATS_DOCKERIZED=1
# Thu, 23 Jan 2025 20:26:12 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 20:26:13 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.25/nats-server-v2.10.25-windows-amd64.zip
# Thu, 23 Jan 2025 20:26:14 GMT
ENV NATS_SERVER_SHASUM=cfc706d1add1d61e7f00023f12ab8e4266f2dddce21ac1cb0934d261d793b185
# Thu, 23 Jan 2025 20:27:37 GMT
RUN Set-PSDebug -Trace 2
# Thu, 23 Jan 2025 20:28:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 23 Jan 2025 20:28:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 23 Jan 2025 20:28:06 GMT
EXPOSE 4222 6222 8222
# Thu, 23 Jan 2025 20:28:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 23 Jan 2025 20:28:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbeaae3c88fdde9250f605077db33243e114005915e5f8089d1fe52db9f7f33`  
		Last Modified: Thu, 23 Jan 2025 20:28:12 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7151274c33714e7509b14b4e0d5b0bb2edc7be2c5c6c367e23da47e5b0fe47e0`  
		Last Modified: Thu, 23 Jan 2025 20:28:12 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be62b080bac43f1250951e5538217700f365c04dbcffcab32948630b1fff874`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8c8166760128743ab6939afcc988275e618e512470c745110922e3c12ec02b`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccd23750ddffcb6549ccf53a46bdbe37f1638a006f0c386ebdef56518ded31c`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4289475cde28eda14db37afc21b3cd5e3e609b9a307fa2adc8e83e35aa5c939a`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 333.1 KB (333123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1770805cfbf8d0508a258a7289fb0322c417cd60a6ae7aba6c6d3e38a45c794`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 6.4 MB (6381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8342c5b961afa372660e90cd752e346589b10235666d4d67c897c2f4e8a7d671`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f571a3f111d510a76501240c7353c3e864c3833c64fc2df499c1351177d39f`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6db5f29326e04b49df5a4c674fd23399c971cece3510aacc7529cd4f1f60d34`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cc47ff9afa1bb9451e9405893d35ad5fed9e2bf17a54a03dca345b2b746bcd`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:b93ef5ffb1f01168b119eaa7d5bd09d06ee4a92b4ca28ec3518b787ebb2549ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:d13ec5ce79a02e1be937820dd36db611e25bd0c08cd9947fa9a5d52a56bf91fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10009883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f82ef16e19c3b28fbf0f9721ceb28da9a34e77fb6f56fafad647123fdeaa12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1389e727b51dad1da0eee4dab424d30b3adc248945c6624b675ac28518cdcf73`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 6.4 MB (6367199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc4d59184023bde8f1163df4dba49dbab7d5ad807a967cb82cc4bdb27ff582`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932199a7e681f9e316441810f9f8a601d6b3024a5f618243b53bcecedcbd26`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a76b53321a9e54c4ae8ac76d4d55092f5344ab9c7a82fc6bf862bb5733d9ac4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a382496dbdb27ac2143007c60c1a2e728f1540254eb46f2b87b08276231356c9`

```dockerfile
```

-	Layers:
	-	`sha256:ce9696da8d1ea1fef5a70bdc0029fd24523875e259b6b3c5d2e29019f972488a`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ed9c796cd3ad56226504a37fdf8d723fb1f733050b8ee6893303fb8430c675b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dfdedee7614113bcdb4520d226d7309166368c268a647cacf4bf5645bd525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da649493a411bfb623f54e86f3b76b40dd7a4bfe42657e83db8d93b71f990f9b`  
		Last Modified: Thu, 23 Jan 2025 20:25:54 GMT  
		Size: 6.0 MB (6017858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb48584554a799af85ef81eb2c395c20e47c0017220a17ea51de65df8274ea`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729c51637a5e23f0df73c5b3934fcf12277ac1f7a7f5c23e554aa98ae0729db`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:97b50584b37c7b333558bd30709d127c88db6736672dcf9acf4358bf8a61e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7f1819c6cba2205ce0b28e6fa6af3c4ca4bfa55deb159eb096942283441b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b47e162ec2703a2ad9bbdef39f28e43c84bdefecd159d4732315024c2d64413`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b5868815b3f528c23a20af1e84c47dd8c3d71b081bec3f282a5080fe0b2123e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9101218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6bd4698025702dc40ccfd1bfa1437953fc9ade0d587ba4e4231ad24d8a7dd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a6b1d44a89dcbf597c9907146e0a51867b4ed4bd2bea7cc517bf93c45e2010`  
		Last Modified: Wed, 08 Jan 2025 18:45:03 GMT  
		Size: 6.0 MB (6003136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca5d46780ac7652092f710b97ba2b37a1c234b0a767343d2041c4bc38b73489`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef8f7a4172b027ce9f98a8732748ade622adb95a4020c38fe9130d0a1d520e1`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ae2683b2444ef44f3dd8ef3e9ea4b2c2cef75fbd2b37f0d12a9ea0948267ac91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6861a34069ee4798adba6258e40dbc34c7d0bbd9cf2df4be451f8bdc77ccda38`

```dockerfile
```

-	Layers:
	-	`sha256:ce68aa0da6eb69d64dcd0cec911721097b7e4db8c1008eb156ed39bb796dee34`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a4da0fc57cf9fbacac471da654b026b79c7f5889a976137434112694c8aa53c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9911663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a90da8fe97e67cfe8003aefeb5e4d496f3c3c2d62b32983346f3e9a71d0ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252a7fd157e5483b31440b7ab2b9dd8fecaa1443ba922c59cc5c0a31e662941`  
		Last Modified: Thu, 23 Jan 2025 20:25:57 GMT  
		Size: 5.9 MB (5918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c75f3d02cf31a351f067d9f29af8eb4e9d19d3cb202055c0d77f5e995a78e`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af341e5640fc20ff58015910ba702a5da4d8c4e86cf39cdd208e9f08e2c46cf8`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d15de15bf8ad9fa5e2d0819628e79168fb40d2ed9ad7d4446c8a3395e5d967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3223335912364a8d57333e693ef24420766757c49743b21adc40203d99a4bd0`

```dockerfile
```

-	Layers:
	-	`sha256:165668ceda68653b6dce0ef8330afde214a7cb42c094103ffd6a6e01835f7b64`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d5552c48e37011850332db8cc1693ec3e9a19234d16767b01bfb170e4c077c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f3e9720f21f14d69795e195215acb5783a4dcd0d766f47739b0251238825c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c646d1e663846cf15c587736bca653e994b2cc7dafa1c5915c0fafac7904392`  
		Last Modified: Thu, 23 Jan 2025 20:26:18 GMT  
		Size: 5.9 MB (5886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7e928a957a1d5442de03b0488186331a62f10c37fa16fa298a4abc86c737c`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddfc69be9741f053b51a5103d25dfaa6f95b62f104c5d3207dec92bfc5f519f`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cf7e706effbc29fca0c819608c4a0f8b3618cabab79f441d8ed0feee9f912e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf338df0b81a0519824480a6b8a7aa51d47848ac769911fa320be6392fad2e64`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf71bd8fdd1f5f4984f86346e93ea054c63b2107a413df819e4111b12b7d3b`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:a2d6f243fa355b743308898df4bedcec37e0ef296d72af3cdbebc87a700e7aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9680027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe977f5917123701c07307dbec905097239eef1be9974c4bf435a9716ebd2f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d56264cbb03f661c76ca48ea4695f8217d7897fc6ddbdbc6f74b5da4e61a620`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 6.2 MB (6212193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c252a87ccdd67c333282abcbcc17c60f67b9428fb3819dcbbad57724ffb313c8`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54677465f2d7d3ad44fe3e538dfab79e5ed4c76fede17650866a6d006c22d6`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:afcb335781617228f17afd454ce4d61c8e8c967ec19b1a648e00102c29a4345d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c7c47650157c85ba3e7f07706a129028c8e17bbd3fa6de2035359e35239b97`

```dockerfile
```

-	Layers:
	-	`sha256:b761dc077830ac087e4440bb5fa6c60ce2505d98fdd146865913031815e3c68f`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.21`

```console
$ docker pull nats@sha256:b93ef5ffb1f01168b119eaa7d5bd09d06ee4a92b4ca28ec3518b787ebb2549ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:d13ec5ce79a02e1be937820dd36db611e25bd0c08cd9947fa9a5d52a56bf91fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10009883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f82ef16e19c3b28fbf0f9721ceb28da9a34e77fb6f56fafad647123fdeaa12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1389e727b51dad1da0eee4dab424d30b3adc248945c6624b675ac28518cdcf73`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 6.4 MB (6367199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc4d59184023bde8f1163df4dba49dbab7d5ad807a967cb82cc4bdb27ff582`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932199a7e681f9e316441810f9f8a601d6b3024a5f618243b53bcecedcbd26`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:a76b53321a9e54c4ae8ac76d4d55092f5344ab9c7a82fc6bf862bb5733d9ac4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a382496dbdb27ac2143007c60c1a2e728f1540254eb46f2b87b08276231356c9`

```dockerfile
```

-	Layers:
	-	`sha256:ce9696da8d1ea1fef5a70bdc0029fd24523875e259b6b3c5d2e29019f972488a`  
		Last Modified: Wed, 08 Jan 2025 18:00:01 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:6ed9c796cd3ad56226504a37fdf8d723fb1f733050b8ee6893303fb8430c675b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1dfdedee7614113bcdb4520d226d7309166368c268a647cacf4bf5645bd525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da649493a411bfb623f54e86f3b76b40dd7a4bfe42657e83db8d93b71f990f9b`  
		Last Modified: Thu, 23 Jan 2025 20:25:54 GMT  
		Size: 6.0 MB (6017858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb48584554a799af85ef81eb2c395c20e47c0017220a17ea51de65df8274ea`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729c51637a5e23f0df73c5b3934fcf12277ac1f7a7f5c23e554aa98ae0729db`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:97b50584b37c7b333558bd30709d127c88db6736672dcf9acf4358bf8a61e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7f1819c6cba2205ce0b28e6fa6af3c4ca4bfa55deb159eb096942283441b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b47e162ec2703a2ad9bbdef39f28e43c84bdefecd159d4732315024c2d64413`  
		Last Modified: Thu, 23 Jan 2025 20:25:53 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:b5868815b3f528c23a20af1e84c47dd8c3d71b081bec3f282a5080fe0b2123e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9101218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6bd4698025702dc40ccfd1bfa1437953fc9ade0d587ba4e4231ad24d8a7dd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a6b1d44a89dcbf597c9907146e0a51867b4ed4bd2bea7cc517bf93c45e2010`  
		Last Modified: Wed, 08 Jan 2025 18:45:03 GMT  
		Size: 6.0 MB (6003136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca5d46780ac7652092f710b97ba2b37a1c234b0a767343d2041c4bc38b73489`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef8f7a4172b027ce9f98a8732748ade622adb95a4020c38fe9130d0a1d520e1`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ae2683b2444ef44f3dd8ef3e9ea4b2c2cef75fbd2b37f0d12a9ea0948267ac91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6861a34069ee4798adba6258e40dbc34c7d0bbd9cf2df4be451f8bdc77ccda38`

```dockerfile
```

-	Layers:
	-	`sha256:ce68aa0da6eb69d64dcd0cec911721097b7e4db8c1008eb156ed39bb796dee34`  
		Last Modified: Wed, 08 Jan 2025 18:45:02 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a4da0fc57cf9fbacac471da654b026b79c7f5889a976137434112694c8aa53c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9911663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a90da8fe97e67cfe8003aefeb5e4d496f3c3c2d62b32983346f3e9a71d0ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252a7fd157e5483b31440b7ab2b9dd8fecaa1443ba922c59cc5c0a31e662941`  
		Last Modified: Thu, 23 Jan 2025 20:25:57 GMT  
		Size: 5.9 MB (5918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67c75f3d02cf31a351f067d9f29af8eb4e9d19d3cb202055c0d77f5e995a78e`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af341e5640fc20ff58015910ba702a5da4d8c4e86cf39cdd208e9f08e2c46cf8`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d15de15bf8ad9fa5e2d0819628e79168fb40d2ed9ad7d4446c8a3395e5d967f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3223335912364a8d57333e693ef24420766757c49743b21adc40203d99a4bd0`

```dockerfile
```

-	Layers:
	-	`sha256:165668ceda68653b6dce0ef8330afde214a7cb42c094103ffd6a6e01835f7b64`  
		Last Modified: Thu, 23 Jan 2025 20:25:56 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:d5552c48e37011850332db8cc1693ec3e9a19234d16767b01bfb170e4c077c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f3e9720f21f14d69795e195215acb5783a4dcd0d766f47739b0251238825c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 18:55:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7e73452331bb348c64ea1029f0fba479c7076db5225b7c76aa0e48671f924e0e' ;; 		armhf) natsArch='arm6'; sha256='f2625f85ba12f92ac32ba9fd1eebb149762bfb56ec1651f84448eb0317f0518d' ;; 		armv7) natsArch='arm7'; sha256='6610744344f3106be8d5b36721ec0498b1715f1fdbc735c005fd3289e7a6bbcc' ;; 		x86_64) natsArch='amd64'; sha256='8a54ebad5f08311257e4267a96c5333ae58667c3ef50a7897bce00e01f6d8d6c' ;; 		x86) natsArch='386'; sha256='567e71796162e568690982afbef058098e2a2c7411beb3a29fc0c75704a6e035' ;; 		s390x) natsArch='s390x'; sha256='d65dc143265517e2162caf7c62926824f093c5b2219edc064576130bdaefe11b' ;; 		ppc64le) natsArch='ppc64le'; sha256='05f7d94c8fa935d6342fafc016ccb904084be518caa2a4e6db7bd0c1863c9d87' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Jan 2025 18:55:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 23 Jan 2025 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 18:55:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c646d1e663846cf15c587736bca653e994b2cc7dafa1c5915c0fafac7904392`  
		Last Modified: Thu, 23 Jan 2025 20:26:18 GMT  
		Size: 5.9 MB (5886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc7e928a957a1d5442de03b0488186331a62f10c37fa16fa298a4abc86c737c`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddfc69be9741f053b51a5103d25dfaa6f95b62f104c5d3207dec92bfc5f519f`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cf7e706effbc29fca0c819608c4a0f8b3618cabab79f441d8ed0feee9f912e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf338df0b81a0519824480a6b8a7aa51d47848ac769911fa320be6392fad2e64`

```dockerfile
```

-	Layers:
	-	`sha256:0ccf71bd8fdd1f5f4984f86346e93ea054c63b2107a413df819e4111b12b7d3b`  
		Last Modified: Thu, 23 Jan 2025 20:26:17 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:a2d6f243fa355b743308898df4bedcec37e0ef296d72af3cdbebc87a700e7aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9680027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe977f5917123701c07307dbec905097239eef1be9974c4bf435a9716ebd2f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 17:21:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a4ae6c46ef545a13a3214bc35696b2806e05b60742f7ed5b2082d3c2f5af854f' ;; 		armhf) natsArch='arm6'; sha256='0061ec69127c1d321af8139a6bdda4e1222a3cfe1ad2654370420734ec735171' ;; 		armv7) natsArch='arm7'; sha256='344d4da46b21291a992a3ed7bbb2ef31539aa7193b6c5936a356be9590b0e961' ;; 		x86_64) natsArch='amd64'; sha256='ee6500f364e3a741b496ae0296c04f2a9d53bbaabac457104ac74596b4a59d85' ;; 		x86) natsArch='386'; sha256='75edd97f98fd0735b2288fb0c0eb6dbceb4e94015390ac4439587fb25ba99044' ;; 		s390x) natsArch='s390x'; sha256='767e2a0f06030ad8c83946e6a5a8718868b88cd5b60958d217d1fdb65024ebae' ;; 		ppc64le) natsArch='ppc64le'; sha256='2c3582f1e9ec7f43e63846d347655035017ca555b33831e13783396774f2d206' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d56264cbb03f661c76ca48ea4695f8217d7897fc6ddbdbc6f74b5da4e61a620`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 6.2 MB (6212193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c252a87ccdd67c333282abcbcc17c60f67b9428fb3819dcbbad57724ffb313c8`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54677465f2d7d3ad44fe3e538dfab79e5ed4c76fede17650866a6d006c22d6`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:afcb335781617228f17afd454ce4d61c8e8c967ec19b1a648e00102c29a4345d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c7c47650157c85ba3e7f07706a129028c8e17bbd3fa6de2035359e35239b97`

```dockerfile
```

-	Layers:
	-	`sha256:b761dc077830ac087e4440bb5fa6c60ce2505d98fdd146865913031815e3c68f`  
		Last Modified: Wed, 08 Jan 2025 18:31:06 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:1f72530645acb97d46973ffbe7b4beb6346b9c55f4a9d36b351e4c6dad753314
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.6775; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:5f9c390b45453cb55529ee7c0ea98f58c9eabbcce148e1fdef04cf8bb9074318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83db84e70fa4a83064757f6f48ae4cd12235da8b6444c70a176a84fff960a37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f2627f3e9adc28bf86cb08c7e382ad970ea899ddc8152bfb60fd5c1fe3d202`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:75e8038c8bbb0b5265cc9122a86bb065eee9d00f5800dae8c6355b8e0a9a745c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c246d72201ffc987cb7434edb7ec9f2b3df97136614b9a40e54756cdb416b72c`

```dockerfile
```

-	Layers:
	-	`sha256:8b34f8855c6dd3c2902d6e451796443e80889b7eb89b66b903756ed07929a167`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:e85e9da7f86adb238cc8a5f7cc45cb0cd87026da70fd44b01e444b8695880f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6e1c8c71ac7babb677e1219162820552049a771bfaf5537fa064fffa339ed7`

```dockerfile
```

-	Layers:
	-	`sha256:e8ae39b919b42a4500939423db63925e2755fca7d061faec83734c4dffc694bf`  
		Last Modified: Thu, 09 Jan 2025 08:57:17 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:81ef7161b07b53e04c4d6f06ff23a819d82edadee1b5114894b84b92bded720a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e573b7356a8dbfa6f0f90b6f1497f8ecba7f2fc930d117eed09b38931f15c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27233802c95930c2c97db1227b08ff00f5b72b607338899c46d31ab86b6bf0dd`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:ecb2bac646bde161319e5d013dd2f9791829f8b7b50df01ea5e10a3279ba3ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3ca0a483861718e290eb7d3e383d11990c2a42ec5980d5659a8df8b26c0671`

```dockerfile
```

-	Layers:
	-	`sha256:9d64b38b227893816e7fee501b8785831fc41177c7da344d2d2efadecdda7a67`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb1f744d45f1644e0a037f18b19e702a46d0eab0646a1e32774a97c1fcb57184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e47297c017006a49499c9dee7f2dd3ef999d9a17436c2c953cbe33bdf5d0c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a726266688ce6f73cf80ad50c512147100f877e50266515a99de500c91b25db3`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:fc4ce673ed5064130d176a89dee2e7643c1bb6407189e6501d3189497186bae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b78f424798237f9dd0e444af21a5fe68199f541753007f102cbd75b9385c2`

```dockerfile
```

-	Layers:
	-	`sha256:111318d590c0977b2a4d6c59b0dc324c853d994ee49032d86aaece1580c4b1c9`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:95f9e2bc23a9b1b10811b86ee1a18a15ee38f77cf56c8910c2a0959012da7e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515e09b78e41cc7926864d6b6e92edc26698a05dcce8dc8aa4a0a025b7c57814`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2024e9028623ac2d4facbfcc79793de84acf606af93e2a58405c55018f61c3`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:44fb1e13792ffab815d9a53fd588385fc17ff1ecc7c8dd52892c212637697274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf8cb760d0ae4538dac4f977b136585f9a3fdbceb692f4bb41893a480cc9782`

```dockerfile
```

-	Layers:
	-	`sha256:d43b7aaceeecac687ad894b912b854ec92c740f29ce3595a404c8b016a36ede2`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:d995fdee651d809102842ddd4f623725fef095e961cd5da9d75f009bcffc6162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31a3e7f0b7232ae529ffc2136b0d5f60df4998428df319d1deffa87afacffa3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b0d648957d541b8618bbb5ede323354ca5ffe9aeb3d1dbc9c352ea097e36a2`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:10560c276ecc00ccc189dd50847ef3dae9a4250913fe911c13361caa0418554d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f6cd92d566df26ed30bfd04e03565d263f2a08a426b5029f4b5b3373dc7fb0`

```dockerfile
```

-	Layers:
	-	`sha256:f9e945fabe7afbcc493bd9ab31004b72d72a266d574fe373fc060704bc2f94a1`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:5f5322bba05b71576e20f209c4b340bd995bdcc31a29a5e40f898e03cd2d591a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161299217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ed26b7d3e8ce4cc01b1be218c7301f56f4ed9c1cef651493d28a2a6204f2dd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 17:50:12 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 Jan 2025 17:50:17 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78be4d7c7554d3cc03be58653079e805ee14881716e7be4da21ed08dc92aecf`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a53c7b6ebfde3e19109bda127b7e6dd65afe79e4f181aff08978e4eeb4f5f35`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 6.0 MB (6025790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43d64cb96be0aa298d48a5812e2c3932f539ffb951d2c5b686e9d942b3ad671`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fff7bbd5ae2661700128fd04b604cfb063ecfefd7316d5f3f135990a00f5f52`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaab287c955c223fb7639ef1c45f7ee8e6cb71fc27b5392944fb1ee749e7aad`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d6ccb426c9a0f0d72f25a723f8c4cfa93a19577d1cb7d21fd99203d4720936`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:9e0236d18c30f44e0cbe71b1976e6465637af55d432cf87fd2dd04546ed19310
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:5f9c390b45453cb55529ee7c0ea98f58c9eabbcce148e1fdef04cf8bb9074318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83db84e70fa4a83064757f6f48ae4cd12235da8b6444c70a176a84fff960a37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f2627f3e9adc28bf86cb08c7e382ad970ea899ddc8152bfb60fd5c1fe3d202`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:75e8038c8bbb0b5265cc9122a86bb065eee9d00f5800dae8c6355b8e0a9a745c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c246d72201ffc987cb7434edb7ec9f2b3df97136614b9a40e54756cdb416b72c`

```dockerfile
```

-	Layers:
	-	`sha256:8b34f8855c6dd3c2902d6e451796443e80889b7eb89b66b903756ed07929a167`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:e85e9da7f86adb238cc8a5f7cc45cb0cd87026da70fd44b01e444b8695880f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6e1c8c71ac7babb677e1219162820552049a771bfaf5537fa064fffa339ed7`

```dockerfile
```

-	Layers:
	-	`sha256:e8ae39b919b42a4500939423db63925e2755fca7d061faec83734c4dffc694bf`  
		Last Modified: Thu, 09 Jan 2025 08:57:17 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:81ef7161b07b53e04c4d6f06ff23a819d82edadee1b5114894b84b92bded720a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e573b7356a8dbfa6f0f90b6f1497f8ecba7f2fc930d117eed09b38931f15c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27233802c95930c2c97db1227b08ff00f5b72b607338899c46d31ab86b6bf0dd`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:ecb2bac646bde161319e5d013dd2f9791829f8b7b50df01ea5e10a3279ba3ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3ca0a483861718e290eb7d3e383d11990c2a42ec5980d5659a8df8b26c0671`

```dockerfile
```

-	Layers:
	-	`sha256:9d64b38b227893816e7fee501b8785831fc41177c7da344d2d2efadecdda7a67`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb1f744d45f1644e0a037f18b19e702a46d0eab0646a1e32774a97c1fcb57184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e47297c017006a49499c9dee7f2dd3ef999d9a17436c2c953cbe33bdf5d0c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a726266688ce6f73cf80ad50c512147100f877e50266515a99de500c91b25db3`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:fc4ce673ed5064130d176a89dee2e7643c1bb6407189e6501d3189497186bae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b78f424798237f9dd0e444af21a5fe68199f541753007f102cbd75b9385c2`

```dockerfile
```

-	Layers:
	-	`sha256:111318d590c0977b2a4d6c59b0dc324c853d994ee49032d86aaece1580c4b1c9`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:95f9e2bc23a9b1b10811b86ee1a18a15ee38f77cf56c8910c2a0959012da7e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515e09b78e41cc7926864d6b6e92edc26698a05dcce8dc8aa4a0a025b7c57814`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2024e9028623ac2d4facbfcc79793de84acf606af93e2a58405c55018f61c3`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:44fb1e13792ffab815d9a53fd588385fc17ff1ecc7c8dd52892c212637697274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf8cb760d0ae4538dac4f977b136585f9a3fdbceb692f4bb41893a480cc9782`

```dockerfile
```

-	Layers:
	-	`sha256:d43b7aaceeecac687ad894b912b854ec92c740f29ce3595a404c8b016a36ede2`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:d995fdee651d809102842ddd4f623725fef095e961cd5da9d75f009bcffc6162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31a3e7f0b7232ae529ffc2136b0d5f60df4998428df319d1deffa87afacffa3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b0d648957d541b8618bbb5ede323354ca5ffe9aeb3d1dbc9c352ea097e36a2`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:10560c276ecc00ccc189dd50847ef3dae9a4250913fe911c13361caa0418554d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f6cd92d566df26ed30bfd04e03565d263f2a08a426b5029f4b5b3373dc7fb0`

```dockerfile
```

-	Layers:
	-	`sha256:f9e945fabe7afbcc493bd9ab31004b72d72a266d574fe373fc060704bc2f94a1`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:57c95a4019f74c260f06f9db81db80a8ee6251cc783f779429765a73bd7b4324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `nats:nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:5f5322bba05b71576e20f209c4b340bd995bdcc31a29a5e40f898e03cd2d591a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161299217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ed26b7d3e8ce4cc01b1be218c7301f56f4ed9c1cef651493d28a2a6204f2dd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 17:50:12 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 Jan 2025 17:50:17 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78be4d7c7554d3cc03be58653079e805ee14881716e7be4da21ed08dc92aecf`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a53c7b6ebfde3e19109bda127b7e6dd65afe79e4f181aff08978e4eeb4f5f35`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 6.0 MB (6025790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43d64cb96be0aa298d48a5812e2c3932f539ffb951d2c5b686e9d942b3ad671`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fff7bbd5ae2661700128fd04b604cfb063ecfefd7316d5f3f135990a00f5f52`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaab287c955c223fb7639ef1c45f7ee8e6cb71fc27b5392944fb1ee749e7aad`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d6ccb426c9a0f0d72f25a723f8c4cfa93a19577d1cb7d21fd99203d4720936`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:57c95a4019f74c260f06f9db81db80a8ee6251cc783f779429765a73bd7b4324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:5f5322bba05b71576e20f209c4b340bd995bdcc31a29a5e40f898e03cd2d591a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161299217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ed26b7d3e8ce4cc01b1be218c7301f56f4ed9c1cef651493d28a2a6204f2dd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 17:50:12 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Wed, 15 Jan 2025 17:50:15 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 15 Jan 2025 17:50:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 15 Jan 2025 17:50:17 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78be4d7c7554d3cc03be58653079e805ee14881716e7be4da21ed08dc92aecf`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a53c7b6ebfde3e19109bda127b7e6dd65afe79e4f181aff08978e4eeb4f5f35`  
		Last Modified: Wed, 15 Jan 2025 17:50:20 GMT  
		Size: 6.0 MB (6025790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43d64cb96be0aa298d48a5812e2c3932f539ffb951d2c5b686e9d942b3ad671`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fff7bbd5ae2661700128fd04b604cfb063ecfefd7316d5f3f135990a00f5f52`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaab287c955c223fb7639ef1c45f7ee8e6cb71fc27b5392944fb1ee749e7aad`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d6ccb426c9a0f0d72f25a723f8c4cfa93a19577d1cb7d21fd99203d4720936`  
		Last Modified: Wed, 15 Jan 2025 17:50:19 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:9e0236d18c30f44e0cbe71b1976e6465637af55d432cf87fd2dd04546ed19310
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:5f9c390b45453cb55529ee7c0ea98f58c9eabbcce148e1fdef04cf8bb9074318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83db84e70fa4a83064757f6f48ae4cd12235da8b6444c70a176a84fff960a37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cb1f9bba9aff495d2f8a23661a6c1c7bc2c839cdc2be180b4b8d9bc9800c45e`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.9 MB (5905148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f2627f3e9adc28bf86cb08c7e382ad970ea899ddc8152bfb60fd5c1fe3d202`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:75e8038c8bbb0b5265cc9122a86bb065eee9d00f5800dae8c6355b8e0a9a745c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c246d72201ffc987cb7434edb7ec9f2b3df97136614b9a40e54756cdb416b72c`

```dockerfile
```

-	Layers:
	-	`sha256:8b34f8855c6dd3c2902d6e451796443e80889b7eb89b66b903756ed07929a167`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f801151009502a85c381ffc3e3d4da1b39a338bd804445dbab92e447a8d0742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5dab6565a7ccd5e8b79dd46bc5519aff76b27bfd17665dd3ab08500446ae12c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:81fd6ecec75a6718f55afc7801f7191a8b41d70739a2651f877929f41efcd454`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.6 MB (5553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4aef5e79acad5215cfeb435fcd7a420447cc550b3045715dcd97efb7cb374f`  
		Last Modified: Tue, 17 Dec 2024 20:07:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e85e9da7f86adb238cc8a5f7cc45cb0cd87026da70fd44b01e444b8695880f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6e1c8c71ac7babb677e1219162820552049a771bfaf5537fa064fffa339ed7`

```dockerfile
```

-	Layers:
	-	`sha256:e8ae39b919b42a4500939423db63925e2755fca7d061faec83734c4dffc694bf`  
		Last Modified: Thu, 09 Jan 2025 08:57:17 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:81ef7161b07b53e04c4d6f06ff23a819d82edadee1b5114894b84b92bded720a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5541947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e573b7356a8dbfa6f0f90b6f1497f8ecba7f2fc930d117eed09b38931f15c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85a1620c1bc6892b5d6c70da117024f4e8fd52994270c35fc7e84782f9682593`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5541438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27233802c95930c2c97db1227b08ff00f5b72b607338899c46d31ab86b6bf0dd`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ecb2bac646bde161319e5d013dd2f9791829f8b7b50df01ea5e10a3279ba3ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3ca0a483861718e290eb7d3e383d11990c2a42ec5980d5659a8df8b26c0671`

```dockerfile
```

-	Layers:
	-	`sha256:9d64b38b227893816e7fee501b8785831fc41177c7da344d2d2efadecdda7a67`  
		Last Modified: Thu, 09 Jan 2025 09:52:54 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb1f744d45f1644e0a037f18b19e702a46d0eab0646a1e32774a97c1fcb57184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e47297c017006a49499c9dee7f2dd3ef999d9a17436c2c953cbe33bdf5d0c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d0b7f1d89d35acbd261abd0ec2bcf54bcc65bb79ebf006850dc5cfae55765a62`  
		Last Modified: Tue, 17 Dec 2024 17:22:54 GMT  
		Size: 5.5 MB (5453688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a726266688ce6f73cf80ad50c512147100f877e50266515a99de500c91b25db3`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:fc4ce673ed5064130d176a89dee2e7643c1bb6407189e6501d3189497186bae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71b78f424798237f9dd0e444af21a5fe68199f541753007f102cbd75b9385c2`

```dockerfile
```

-	Layers:
	-	`sha256:111318d590c0977b2a4d6c59b0dc324c853d994ee49032d86aaece1580c4b1c9`  
		Last Modified: Thu, 09 Jan 2025 06:32:57 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:95f9e2bc23a9b1b10811b86ee1a18a15ee38f77cf56c8910c2a0959012da7e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515e09b78e41cc7926864d6b6e92edc26698a05dcce8dc8aa4a0a025b7c57814`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72b285162443e680327c1bf58de30e30459f3f8193b0769fd1fad6f4f115b124`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2024e9028623ac2d4facbfcc79793de84acf606af93e2a58405c55018f61c3`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:44fb1e13792ffab815d9a53fd588385fc17ff1ecc7c8dd52892c212637697274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf8cb760d0ae4538dac4f977b136585f9a3fdbceb692f4bb41893a480cc9782`

```dockerfile
```

-	Layers:
	-	`sha256:d43b7aaceeecac687ad894b912b854ec92c740f29ce3595a404c8b016a36ede2`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:d995fdee651d809102842ddd4f623725fef095e961cd5da9d75f009bcffc6162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31a3e7f0b7232ae529ffc2136b0d5f60df4998428df319d1deffa87afacffa3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 17 Dec 2024 17:21:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 17 Dec 2024 17:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 17 Dec 2024 17:21:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 17 Dec 2024 17:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd4119cb6f8c6b49f3ec55933200d2283d0f58b8b79bb753e5436770b7c2b320`  
		Last Modified: Tue, 17 Dec 2024 17:22:57 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b0d648957d541b8618bbb5ede323354ca5ffe9aeb3d1dbc9c352ea097e36a2`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:10560c276ecc00ccc189dd50847ef3dae9a4250913fe911c13361caa0418554d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f6cd92d566df26ed30bfd04e03565d263f2a08a426b5029f4b5b3373dc7fb0`

```dockerfile
```

-	Layers:
	-	`sha256:f9e945fabe7afbcc493bd9ab31004b72d72a266d574fe373fc060704bc2f94a1`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:521666e383ff922ceb42fcda89d151092f909f6e1b07869e152e6fed707d9873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `nats:windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:4d0d68cf2f42b99731c82c9ae9fefde7da5d6603a050421c29f7f82e574dcc21
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128939081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71502b69ef80233acfce527fd9ee52d7af303fb5d8fbf153dacb04bab44baf26`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 20:26:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jan 2025 20:26:12 GMT
ENV NATS_DOCKERIZED=1
# Thu, 23 Jan 2025 20:26:12 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 20:26:13 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.25/nats-server-v2.10.25-windows-amd64.zip
# Thu, 23 Jan 2025 20:26:14 GMT
ENV NATS_SERVER_SHASUM=cfc706d1add1d61e7f00023f12ab8e4266f2dddce21ac1cb0934d261d793b185
# Thu, 23 Jan 2025 20:27:37 GMT
RUN Set-PSDebug -Trace 2
# Thu, 23 Jan 2025 20:28:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 23 Jan 2025 20:28:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 23 Jan 2025 20:28:06 GMT
EXPOSE 4222 6222 8222
# Thu, 23 Jan 2025 20:28:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 23 Jan 2025 20:28:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbeaae3c88fdde9250f605077db33243e114005915e5f8089d1fe52db9f7f33`  
		Last Modified: Thu, 23 Jan 2025 20:28:12 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7151274c33714e7509b14b4e0d5b0bb2edc7be2c5c6c367e23da47e5b0fe47e0`  
		Last Modified: Thu, 23 Jan 2025 20:28:12 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be62b080bac43f1250951e5538217700f365c04dbcffcab32948630b1fff874`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8c8166760128743ab6939afcc988275e618e512470c745110922e3c12ec02b`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccd23750ddffcb6549ccf53a46bdbe37f1638a006f0c386ebdef56518ded31c`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4289475cde28eda14db37afc21b3cd5e3e609b9a307fa2adc8e83e35aa5c939a`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 333.1 KB (333123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1770805cfbf8d0508a258a7289fb0322c417cd60a6ae7aba6c6d3e38a45c794`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 6.4 MB (6381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8342c5b961afa372660e90cd752e346589b10235666d4d67c897c2f4e8a7d671`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f571a3f111d510a76501240c7353c3e864c3833c64fc2df499c1351177d39f`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6db5f29326e04b49df5a4c674fd23399c971cece3510aacc7529cd4f1f60d34`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cc47ff9afa1bb9451e9405893d35ad5fed9e2bf17a54a03dca345b2b746bcd`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:521666e383ff922ceb42fcda89d151092f909f6e1b07869e152e6fed707d9873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull nats@sha256:4d0d68cf2f42b99731c82c9ae9fefde7da5d6603a050421c29f7f82e574dcc21
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128939081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71502b69ef80233acfce527fd9ee52d7af303fb5d8fbf153dacb04bab44baf26`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 20:26:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 23 Jan 2025 20:26:12 GMT
ENV NATS_DOCKERIZED=1
# Thu, 23 Jan 2025 20:26:12 GMT
ENV NATS_SERVER=2.10.25
# Thu, 23 Jan 2025 20:26:13 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.25/nats-server-v2.10.25-windows-amd64.zip
# Thu, 23 Jan 2025 20:26:14 GMT
ENV NATS_SERVER_SHASUM=cfc706d1add1d61e7f00023f12ab8e4266f2dddce21ac1cb0934d261d793b185
# Thu, 23 Jan 2025 20:27:37 GMT
RUN Set-PSDebug -Trace 2
# Thu, 23 Jan 2025 20:28:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 23 Jan 2025 20:28:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 23 Jan 2025 20:28:06 GMT
EXPOSE 4222 6222 8222
# Thu, 23 Jan 2025 20:28:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 23 Jan 2025 20:28:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbeaae3c88fdde9250f605077db33243e114005915e5f8089d1fe52db9f7f33`  
		Last Modified: Thu, 23 Jan 2025 20:28:12 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7151274c33714e7509b14b4e0d5b0bb2edc7be2c5c6c367e23da47e5b0fe47e0`  
		Last Modified: Thu, 23 Jan 2025 20:28:12 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be62b080bac43f1250951e5538217700f365c04dbcffcab32948630b1fff874`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8c8166760128743ab6939afcc988275e618e512470c745110922e3c12ec02b`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccd23750ddffcb6549ccf53a46bdbe37f1638a006f0c386ebdef56518ded31c`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4289475cde28eda14db37afc21b3cd5e3e609b9a307fa2adc8e83e35aa5c939a`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 333.1 KB (333123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1770805cfbf8d0508a258a7289fb0322c417cd60a6ae7aba6c6d3e38a45c794`  
		Last Modified: Thu, 23 Jan 2025 20:28:11 GMT  
		Size: 6.4 MB (6381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8342c5b961afa372660e90cd752e346589b10235666d4d67c897c2f4e8a7d671`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f571a3f111d510a76501240c7353c3e864c3833c64fc2df499c1351177d39f`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6db5f29326e04b49df5a4c674fd23399c971cece3510aacc7529cd4f1f60d34`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cc47ff9afa1bb9451e9405893d35ad5fed9e2bf17a54a03dca345b2b746bcd`  
		Last Modified: Thu, 23 Jan 2025 20:28:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
