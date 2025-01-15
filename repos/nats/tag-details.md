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
-	[`nats:2.10.24`](#nats21024)
-	[`nats:2.10.24-alpine`](#nats21024-alpine)
-	[`nats:2.10.24-alpine3.21`](#nats21024-alpine321)
-	[`nats:2.10.24-linux`](#nats21024-linux)
-	[`nats:2.10.24-nanoserver`](#nats21024-nanoserver)
-	[`nats:2.10.24-nanoserver-1809`](#nats21024-nanoserver-1809)
-	[`nats:2.10.24-scratch`](#nats21024-scratch)
-	[`nats:2.10.24-windowsservercore`](#nats21024-windowsservercore)
-	[`nats:2.10.24-windowsservercore-1809`](#nats21024-windowsservercore-1809)
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
$ docker pull nats@sha256:e7fb72b546e897024123450c257a5874d3625a48e17adcb8de234cb202a9cdcc
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
	-	windows version 10.0.17763.6659; amd64

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
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:47 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:38 GMT  
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

### `nats:2` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Fri, 13 Dec 2024 15:43:11 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Wed, 18 Dec 2024 00:00:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:fd981e2ab99000964bd15286054e61fcc445732fd907db039f260fc0b824b314
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
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:44:42 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:433eace2afe3116663501e605137b1342e594cacdb6966f39a4d0df268bf1db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9377176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5e4870785bb8d3ce233f8e51d75b3c836d532a4b108a10ec5b904eece338a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf930c71ea8a206b4086d5c226d0bb29b91312f4ba0fb5686ed213131f7c1fce`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 6.0 MB (6012322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3eae10f614d94a7bcc2f8da2f396371afed6fcf19a2a0fa09912e2a8928d16`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac55c9747f66c4223ad92350b9c2f4ae632289aa54c0896ff2c4bfb51fe226c`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e926308a529ca3df71bab310384933d7494a7b9dbd5a1c19897bc8d0ac96d7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9cda5cb22de22806f653121b4f4280e163cfeb76c7bda813be4a23180c799d`

```dockerfile
```

-	Layers:
	-	`sha256:443e6c2877a7f9af9e85b02786a2cd315d99fd6081a70794d949cfa9b32df2d6`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 14.4 KB (14430 bytes)  
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
$ docker pull nats@sha256:06f83448f3998be4a3663bb016818a5e77a0dabc0b7e4cde4631b7229e9bc051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9908604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d31bd54bf304ebf7853a6da58b3a77e56942fc898c6bee4f3aeac90fe7146db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2319f4b861d20d91a79cb0b31fa138c4fa0f0e8e0f1d48241f67e8057aebae3`  
		Last Modified: Wed, 08 Jan 2025 18:43:13 GMT  
		Size: 5.9 MB (5915276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18be591190612e251286e917fa3eb6f615be7aa9bea5c411422a8e2c94100b9b`  
		Last Modified: Wed, 08 Jan 2025 18:43:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43aededc0983f2e468a526a5a2c0ce30a0094b60a0e5436abf152cac39ad4301`  
		Last Modified: Tue, 14 Jan 2025 20:54:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1e6852827907d03087f78ba2499420258c71c556f679ebee85b527c6d44bfb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c084013fe4a7c0717ee95605f965902e8757de29f4ac5654e97d94b44157b1`

```dockerfile
```

-	Layers:
	-	`sha256:8a790b3bd9ae36824a545f0b1cf838d02166e5d54a3f2fc640990a4c6e839992`  
		Last Modified: Wed, 08 Jan 2025 18:43:12 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:dba35cd86f317f0d4890697bfc5958af2ce36b261fb47d6ee7c6a0b329413e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9456147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6519bc2a29fc7004298799e4cdd113cb764aae1d8b829b72798b48740283cda3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083843bb209f63812a31ab46fe5bcf0253b9604abe5cd0b2f567e6ec9b5c0d1a`  
		Last Modified: Wed, 08 Jan 2025 18:29:05 GMT  
		Size: 5.9 MB (5881578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1278fab8bd865c13254e886eebbdf15b221951118726df5d7ecc1d28c895a590`  
		Last Modified: Wed, 08 Jan 2025 18:29:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6213e9bcfdb590de78a8793596ccd78d7d3e1338c2f0f51dd766df6fccbd920e`  
		Last Modified: Wed, 08 Jan 2025 18:29:04 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:fef206b3ac985104e9f09104765e0ae2a08cf617b2d535be1313154cb37f5639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cdbb6ac4ec6162f10bfeed21eb48f3b7fe5ae64c6faee116ccd9a5931cb690`

```dockerfile
```

-	Layers:
	-	`sha256:e9703e3c1a1be9e27bbc9ae51c1fb1b834ebb3761163483df2853f9a5dbfe36c`  
		Last Modified: Wed, 08 Jan 2025 18:29:04 GMT  
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
$ docker pull nats@sha256:fd981e2ab99000964bd15286054e61fcc445732fd907db039f260fc0b824b314
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
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:44:42 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:433eace2afe3116663501e605137b1342e594cacdb6966f39a4d0df268bf1db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9377176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5e4870785bb8d3ce233f8e51d75b3c836d532a4b108a10ec5b904eece338a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf930c71ea8a206b4086d5c226d0bb29b91312f4ba0fb5686ed213131f7c1fce`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 6.0 MB (6012322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3eae10f614d94a7bcc2f8da2f396371afed6fcf19a2a0fa09912e2a8928d16`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac55c9747f66c4223ad92350b9c2f4ae632289aa54c0896ff2c4bfb51fe226c`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:e926308a529ca3df71bab310384933d7494a7b9dbd5a1c19897bc8d0ac96d7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9cda5cb22de22806f653121b4f4280e163cfeb76c7bda813be4a23180c799d`

```dockerfile
```

-	Layers:
	-	`sha256:443e6c2877a7f9af9e85b02786a2cd315d99fd6081a70794d949cfa9b32df2d6`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 14.4 KB (14430 bytes)  
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
$ docker pull nats@sha256:06f83448f3998be4a3663bb016818a5e77a0dabc0b7e4cde4631b7229e9bc051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9908604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d31bd54bf304ebf7853a6da58b3a77e56942fc898c6bee4f3aeac90fe7146db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2319f4b861d20d91a79cb0b31fa138c4fa0f0e8e0f1d48241f67e8057aebae3`  
		Last Modified: Wed, 08 Jan 2025 18:43:13 GMT  
		Size: 5.9 MB (5915276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18be591190612e251286e917fa3eb6f615be7aa9bea5c411422a8e2c94100b9b`  
		Last Modified: Wed, 08 Jan 2025 18:43:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43aededc0983f2e468a526a5a2c0ce30a0094b60a0e5436abf152cac39ad4301`  
		Last Modified: Tue, 14 Jan 2025 20:54:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:1e6852827907d03087f78ba2499420258c71c556f679ebee85b527c6d44bfb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c084013fe4a7c0717ee95605f965902e8757de29f4ac5654e97d94b44157b1`

```dockerfile
```

-	Layers:
	-	`sha256:8a790b3bd9ae36824a545f0b1cf838d02166e5d54a3f2fc640990a4c6e839992`  
		Last Modified: Wed, 08 Jan 2025 18:43:12 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:dba35cd86f317f0d4890697bfc5958af2ce36b261fb47d6ee7c6a0b329413e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9456147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6519bc2a29fc7004298799e4cdd113cb764aae1d8b829b72798b48740283cda3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083843bb209f63812a31ab46fe5bcf0253b9604abe5cd0b2f567e6ec9b5c0d1a`  
		Last Modified: Wed, 08 Jan 2025 18:29:05 GMT  
		Size: 5.9 MB (5881578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1278fab8bd865c13254e886eebbdf15b221951118726df5d7ecc1d28c895a590`  
		Last Modified: Wed, 08 Jan 2025 18:29:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6213e9bcfdb590de78a8793596ccd78d7d3e1338c2f0f51dd766df6fccbd920e`  
		Last Modified: Wed, 08 Jan 2025 18:29:04 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:fef206b3ac985104e9f09104765e0ae2a08cf617b2d535be1313154cb37f5639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cdbb6ac4ec6162f10bfeed21eb48f3b7fe5ae64c6faee116ccd9a5931cb690`

```dockerfile
```

-	Layers:
	-	`sha256:e9703e3c1a1be9e27bbc9ae51c1fb1b834ebb3761163483df2853f9a5dbfe36c`  
		Last Modified: Wed, 08 Jan 2025 18:29:04 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:47 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:38 GMT  
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
$ docker pull nats@sha256:37e1b8a8d0e258480f2b4e3e528c51625f7c66283ec06ca04228db3a08fa024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Fri, 13 Dec 2024 15:43:11 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Wed, 18 Dec 2024 00:00:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:37e1b8a8d0e258480f2b4e3e528c51625f7c66283ec06ca04228db3a08fa024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Fri, 13 Dec 2024 15:43:11 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Wed, 18 Dec 2024 00:00:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
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
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:47 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:38 GMT  
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
$ docker pull nats@sha256:358028020ee9c6b6ff8494f70ecbfddddf5b29d36bd20ec1b9b37eb351c46081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:c6e3358af2d309d6c2ed2c4321b8d16f0c8c2b817d67b61e77790abeab192882
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64938b4574dd9f4d28b0fdba70a6f3483c75359cd4de6fe307eaf6b4c9e6c5d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 17 Dec 2024 19:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Dec 2024 19:28:54 GMT
ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 19:28:55 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 19:28:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.24/nats-server-v2.10.24-windows-amd64.zip
# Tue, 17 Dec 2024 19:28:57 GMT
ENV NATS_SERVER_SHASUM=bf94c9a9f1685147fd95f6c62f26d16fb72dc8c8c592e2d8c9115e2491c508c3
# Tue, 17 Dec 2024 19:30:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 17 Dec 2024 19:31:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 17 Dec 2024 19:31:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 19:31:06 GMT
EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 19:31:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 19:31:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995e898d38ff13b74b2bf42182403105bd564ca1c8cd3c2bccadac08c8172ca2`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f7d745fbcac3f49a978704fb067848ad5982ff0f7f116bfaceb8e9c68fbc7`  
		Last Modified: Wed, 18 Dec 2024 10:08:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a5927c302d6e5e93a6570c06c06ce9862ef400bd5fea534fea403fd76e9b8`  
		Last Modified: Mon, 06 Jan 2025 17:53:46 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e7b1cd8a1d4aa5917755e9a51eb72256b93ddf6aa3825cbd84213d86f046d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a76e8a87993daefe8a56da532e9ecac69a46fe935f34deac5f3e2ccff312c7`  
		Last Modified: Mon, 06 Jan 2025 19:55:37 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f37de67167c5db5acc1c6ba5c9f86ac4f699f4c646ecae8bccaaa2a6b86bb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:14 GMT  
		Size: 465.9 KB (465852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125faf71663c9c259588da9545dcfc1d961e59d92ce5a9486c7d389cb61bc2c`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 6.4 MB (6375751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9b5ddb5fe65a52ed1c161189ff40d0273af9d50a8a6777a98abffd5b4f7d0`  
		Last Modified: Wed, 18 Dec 2024 00:00:14 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6b8c72206232edf4922cfb68939224b12d0d8eb8e2e4c88e5e66875586d0b`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ec3b766844bacc1ba6a7d126a373851ec2b899f045cddd539bc7f1f7ffbd6`  
		Last Modified: Tue, 07 Jan 2025 03:47:10 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d656e63d77c756e50abf1d5d895ac8c06814dd594cc1bf16ea92894907949e`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:358028020ee9c6b6ff8494f70ecbfddddf5b29d36bd20ec1b9b37eb351c46081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:c6e3358af2d309d6c2ed2c4321b8d16f0c8c2b817d67b61e77790abeab192882
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64938b4574dd9f4d28b0fdba70a6f3483c75359cd4de6fe307eaf6b4c9e6c5d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 17 Dec 2024 19:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Dec 2024 19:28:54 GMT
ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 19:28:55 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 19:28:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.24/nats-server-v2.10.24-windows-amd64.zip
# Tue, 17 Dec 2024 19:28:57 GMT
ENV NATS_SERVER_SHASUM=bf94c9a9f1685147fd95f6c62f26d16fb72dc8c8c592e2d8c9115e2491c508c3
# Tue, 17 Dec 2024 19:30:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 17 Dec 2024 19:31:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 17 Dec 2024 19:31:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 19:31:06 GMT
EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 19:31:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 19:31:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995e898d38ff13b74b2bf42182403105bd564ca1c8cd3c2bccadac08c8172ca2`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f7d745fbcac3f49a978704fb067848ad5982ff0f7f116bfaceb8e9c68fbc7`  
		Last Modified: Wed, 18 Dec 2024 10:08:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a5927c302d6e5e93a6570c06c06ce9862ef400bd5fea534fea403fd76e9b8`  
		Last Modified: Mon, 06 Jan 2025 17:53:46 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e7b1cd8a1d4aa5917755e9a51eb72256b93ddf6aa3825cbd84213d86f046d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a76e8a87993daefe8a56da532e9ecac69a46fe935f34deac5f3e2ccff312c7`  
		Last Modified: Mon, 06 Jan 2025 19:55:37 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f37de67167c5db5acc1c6ba5c9f86ac4f699f4c646ecae8bccaaa2a6b86bb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:14 GMT  
		Size: 465.9 KB (465852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125faf71663c9c259588da9545dcfc1d961e59d92ce5a9486c7d389cb61bc2c`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 6.4 MB (6375751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9b5ddb5fe65a52ed1c161189ff40d0273af9d50a8a6777a98abffd5b4f7d0`  
		Last Modified: Wed, 18 Dec 2024 00:00:14 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6b8c72206232edf4922cfb68939224b12d0d8eb8e2e4c88e5e66875586d0b`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ec3b766844bacc1ba6a7d126a373851ec2b899f045cddd539bc7f1f7ffbd6`  
		Last Modified: Tue, 07 Jan 2025 03:47:10 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d656e63d77c756e50abf1d5d895ac8c06814dd594cc1bf16ea92894907949e`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:e7fb72b546e897024123450c257a5874d3625a48e17adcb8de234cb202a9cdcc
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
	-	windows version 10.0.17763.6659; amd64

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
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:47 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:38 GMT  
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

### `nats:2.10` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Fri, 13 Dec 2024 15:43:11 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Wed, 18 Dec 2024 00:00:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:fd981e2ab99000964bd15286054e61fcc445732fd907db039f260fc0b824b314
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
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:44:42 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:433eace2afe3116663501e605137b1342e594cacdb6966f39a4d0df268bf1db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9377176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5e4870785bb8d3ce233f8e51d75b3c836d532a4b108a10ec5b904eece338a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf930c71ea8a206b4086d5c226d0bb29b91312f4ba0fb5686ed213131f7c1fce`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 6.0 MB (6012322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3eae10f614d94a7bcc2f8da2f396371afed6fcf19a2a0fa09912e2a8928d16`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac55c9747f66c4223ad92350b9c2f4ae632289aa54c0896ff2c4bfb51fe226c`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e926308a529ca3df71bab310384933d7494a7b9dbd5a1c19897bc8d0ac96d7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9cda5cb22de22806f653121b4f4280e163cfeb76c7bda813be4a23180c799d`

```dockerfile
```

-	Layers:
	-	`sha256:443e6c2877a7f9af9e85b02786a2cd315d99fd6081a70794d949cfa9b32df2d6`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 14.4 KB (14430 bytes)  
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
$ docker pull nats@sha256:06f83448f3998be4a3663bb016818a5e77a0dabc0b7e4cde4631b7229e9bc051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9908604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d31bd54bf304ebf7853a6da58b3a77e56942fc898c6bee4f3aeac90fe7146db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2319f4b861d20d91a79cb0b31fa138c4fa0f0e8e0f1d48241f67e8057aebae3`  
		Last Modified: Wed, 08 Jan 2025 18:43:13 GMT  
		Size: 5.9 MB (5915276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18be591190612e251286e917fa3eb6f615be7aa9bea5c411422a8e2c94100b9b`  
		Last Modified: Wed, 08 Jan 2025 18:43:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43aededc0983f2e468a526a5a2c0ce30a0094b60a0e5436abf152cac39ad4301`  
		Last Modified: Tue, 14 Jan 2025 20:54:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1e6852827907d03087f78ba2499420258c71c556f679ebee85b527c6d44bfb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c084013fe4a7c0717ee95605f965902e8757de29f4ac5654e97d94b44157b1`

```dockerfile
```

-	Layers:
	-	`sha256:8a790b3bd9ae36824a545f0b1cf838d02166e5d54a3f2fc640990a4c6e839992`  
		Last Modified: Wed, 08 Jan 2025 18:43:12 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:dba35cd86f317f0d4890697bfc5958af2ce36b261fb47d6ee7c6a0b329413e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9456147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6519bc2a29fc7004298799e4cdd113cb764aae1d8b829b72798b48740283cda3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083843bb209f63812a31ab46fe5bcf0253b9604abe5cd0b2f567e6ec9b5c0d1a`  
		Last Modified: Wed, 08 Jan 2025 18:29:05 GMT  
		Size: 5.9 MB (5881578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1278fab8bd865c13254e886eebbdf15b221951118726df5d7ecc1d28c895a590`  
		Last Modified: Wed, 08 Jan 2025 18:29:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6213e9bcfdb590de78a8793596ccd78d7d3e1338c2f0f51dd766df6fccbd920e`  
		Last Modified: Wed, 08 Jan 2025 18:29:04 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:fef206b3ac985104e9f09104765e0ae2a08cf617b2d535be1313154cb37f5639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cdbb6ac4ec6162f10bfeed21eb48f3b7fe5ae64c6faee116ccd9a5931cb690`

```dockerfile
```

-	Layers:
	-	`sha256:e9703e3c1a1be9e27bbc9ae51c1fb1b834ebb3761163483df2853f9a5dbfe36c`  
		Last Modified: Wed, 08 Jan 2025 18:29:04 GMT  
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
$ docker pull nats@sha256:fd981e2ab99000964bd15286054e61fcc445732fd907db039f260fc0b824b314
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
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:44:42 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:433eace2afe3116663501e605137b1342e594cacdb6966f39a4d0df268bf1db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9377176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5e4870785bb8d3ce233f8e51d75b3c836d532a4b108a10ec5b904eece338a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf930c71ea8a206b4086d5c226d0bb29b91312f4ba0fb5686ed213131f7c1fce`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 6.0 MB (6012322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3eae10f614d94a7bcc2f8da2f396371afed6fcf19a2a0fa09912e2a8928d16`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac55c9747f66c4223ad92350b9c2f4ae632289aa54c0896ff2c4bfb51fe226c`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:e926308a529ca3df71bab310384933d7494a7b9dbd5a1c19897bc8d0ac96d7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9cda5cb22de22806f653121b4f4280e163cfeb76c7bda813be4a23180c799d`

```dockerfile
```

-	Layers:
	-	`sha256:443e6c2877a7f9af9e85b02786a2cd315d99fd6081a70794d949cfa9b32df2d6`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 14.4 KB (14430 bytes)  
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
$ docker pull nats@sha256:06f83448f3998be4a3663bb016818a5e77a0dabc0b7e4cde4631b7229e9bc051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9908604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d31bd54bf304ebf7853a6da58b3a77e56942fc898c6bee4f3aeac90fe7146db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2319f4b861d20d91a79cb0b31fa138c4fa0f0e8e0f1d48241f67e8057aebae3`  
		Last Modified: Wed, 08 Jan 2025 18:43:13 GMT  
		Size: 5.9 MB (5915276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18be591190612e251286e917fa3eb6f615be7aa9bea5c411422a8e2c94100b9b`  
		Last Modified: Wed, 08 Jan 2025 18:43:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43aededc0983f2e468a526a5a2c0ce30a0094b60a0e5436abf152cac39ad4301`  
		Last Modified: Tue, 14 Jan 2025 20:54:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:1e6852827907d03087f78ba2499420258c71c556f679ebee85b527c6d44bfb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c084013fe4a7c0717ee95605f965902e8757de29f4ac5654e97d94b44157b1`

```dockerfile
```

-	Layers:
	-	`sha256:8a790b3bd9ae36824a545f0b1cf838d02166e5d54a3f2fc640990a4c6e839992`  
		Last Modified: Wed, 08 Jan 2025 18:43:12 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:dba35cd86f317f0d4890697bfc5958af2ce36b261fb47d6ee7c6a0b329413e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9456147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6519bc2a29fc7004298799e4cdd113cb764aae1d8b829b72798b48740283cda3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083843bb209f63812a31ab46fe5bcf0253b9604abe5cd0b2f567e6ec9b5c0d1a`  
		Last Modified: Wed, 08 Jan 2025 18:29:05 GMT  
		Size: 5.9 MB (5881578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1278fab8bd865c13254e886eebbdf15b221951118726df5d7ecc1d28c895a590`  
		Last Modified: Wed, 08 Jan 2025 18:29:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6213e9bcfdb590de78a8793596ccd78d7d3e1338c2f0f51dd766df6fccbd920e`  
		Last Modified: Wed, 08 Jan 2025 18:29:04 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:fef206b3ac985104e9f09104765e0ae2a08cf617b2d535be1313154cb37f5639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cdbb6ac4ec6162f10bfeed21eb48f3b7fe5ae64c6faee116ccd9a5931cb690`

```dockerfile
```

-	Layers:
	-	`sha256:e9703e3c1a1be9e27bbc9ae51c1fb1b834ebb3761163483df2853f9a5dbfe36c`  
		Last Modified: Wed, 08 Jan 2025 18:29:04 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:47 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:38 GMT  
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
$ docker pull nats@sha256:37e1b8a8d0e258480f2b4e3e528c51625f7c66283ec06ca04228db3a08fa024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Fri, 13 Dec 2024 15:43:11 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Wed, 18 Dec 2024 00:00:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:37e1b8a8d0e258480f2b4e3e528c51625f7c66283ec06ca04228db3a08fa024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Fri, 13 Dec 2024 15:43:11 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Wed, 18 Dec 2024 00:00:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
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
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:47 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:38 GMT  
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
$ docker pull nats@sha256:358028020ee9c6b6ff8494f70ecbfddddf5b29d36bd20ec1b9b37eb351c46081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:c6e3358af2d309d6c2ed2c4321b8d16f0c8c2b817d67b61e77790abeab192882
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64938b4574dd9f4d28b0fdba70a6f3483c75359cd4de6fe307eaf6b4c9e6c5d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 17 Dec 2024 19:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Dec 2024 19:28:54 GMT
ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 19:28:55 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 19:28:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.24/nats-server-v2.10.24-windows-amd64.zip
# Tue, 17 Dec 2024 19:28:57 GMT
ENV NATS_SERVER_SHASUM=bf94c9a9f1685147fd95f6c62f26d16fb72dc8c8c592e2d8c9115e2491c508c3
# Tue, 17 Dec 2024 19:30:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 17 Dec 2024 19:31:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 17 Dec 2024 19:31:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 19:31:06 GMT
EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 19:31:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 19:31:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995e898d38ff13b74b2bf42182403105bd564ca1c8cd3c2bccadac08c8172ca2`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f7d745fbcac3f49a978704fb067848ad5982ff0f7f116bfaceb8e9c68fbc7`  
		Last Modified: Wed, 18 Dec 2024 10:08:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a5927c302d6e5e93a6570c06c06ce9862ef400bd5fea534fea403fd76e9b8`  
		Last Modified: Mon, 06 Jan 2025 17:53:46 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e7b1cd8a1d4aa5917755e9a51eb72256b93ddf6aa3825cbd84213d86f046d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a76e8a87993daefe8a56da532e9ecac69a46fe935f34deac5f3e2ccff312c7`  
		Last Modified: Mon, 06 Jan 2025 19:55:37 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f37de67167c5db5acc1c6ba5c9f86ac4f699f4c646ecae8bccaaa2a6b86bb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:14 GMT  
		Size: 465.9 KB (465852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125faf71663c9c259588da9545dcfc1d961e59d92ce5a9486c7d389cb61bc2c`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 6.4 MB (6375751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9b5ddb5fe65a52ed1c161189ff40d0273af9d50a8a6777a98abffd5b4f7d0`  
		Last Modified: Wed, 18 Dec 2024 00:00:14 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6b8c72206232edf4922cfb68939224b12d0d8eb8e2e4c88e5e66875586d0b`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ec3b766844bacc1ba6a7d126a373851ec2b899f045cddd539bc7f1f7ffbd6`  
		Last Modified: Tue, 07 Jan 2025 03:47:10 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d656e63d77c756e50abf1d5d895ac8c06814dd594cc1bf16ea92894907949e`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:358028020ee9c6b6ff8494f70ecbfddddf5b29d36bd20ec1b9b37eb351c46081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:c6e3358af2d309d6c2ed2c4321b8d16f0c8c2b817d67b61e77790abeab192882
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64938b4574dd9f4d28b0fdba70a6f3483c75359cd4de6fe307eaf6b4c9e6c5d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 17 Dec 2024 19:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Dec 2024 19:28:54 GMT
ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 19:28:55 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 19:28:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.24/nats-server-v2.10.24-windows-amd64.zip
# Tue, 17 Dec 2024 19:28:57 GMT
ENV NATS_SERVER_SHASUM=bf94c9a9f1685147fd95f6c62f26d16fb72dc8c8c592e2d8c9115e2491c508c3
# Tue, 17 Dec 2024 19:30:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 17 Dec 2024 19:31:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 17 Dec 2024 19:31:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 19:31:06 GMT
EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 19:31:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 19:31:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995e898d38ff13b74b2bf42182403105bd564ca1c8cd3c2bccadac08c8172ca2`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f7d745fbcac3f49a978704fb067848ad5982ff0f7f116bfaceb8e9c68fbc7`  
		Last Modified: Wed, 18 Dec 2024 10:08:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a5927c302d6e5e93a6570c06c06ce9862ef400bd5fea534fea403fd76e9b8`  
		Last Modified: Mon, 06 Jan 2025 17:53:46 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e7b1cd8a1d4aa5917755e9a51eb72256b93ddf6aa3825cbd84213d86f046d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a76e8a87993daefe8a56da532e9ecac69a46fe935f34deac5f3e2ccff312c7`  
		Last Modified: Mon, 06 Jan 2025 19:55:37 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f37de67167c5db5acc1c6ba5c9f86ac4f699f4c646ecae8bccaaa2a6b86bb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:14 GMT  
		Size: 465.9 KB (465852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125faf71663c9c259588da9545dcfc1d961e59d92ce5a9486c7d389cb61bc2c`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 6.4 MB (6375751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9b5ddb5fe65a52ed1c161189ff40d0273af9d50a8a6777a98abffd5b4f7d0`  
		Last Modified: Wed, 18 Dec 2024 00:00:14 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6b8c72206232edf4922cfb68939224b12d0d8eb8e2e4c88e5e66875586d0b`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ec3b766844bacc1ba6a7d126a373851ec2b899f045cddd539bc7f1f7ffbd6`  
		Last Modified: Tue, 07 Jan 2025 03:47:10 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d656e63d77c756e50abf1d5d895ac8c06814dd594cc1bf16ea92894907949e`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.24`

```console
$ docker pull nats@sha256:e7fb72b546e897024123450c257a5874d3625a48e17adcb8de234cb202a9cdcc
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
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10.24` - linux; amd64

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

### `nats:2.10.24` - unknown; unknown

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

### `nats:2.10.24` - linux; arm variant v6

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

### `nats:2.10.24` - unknown; unknown

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

### `nats:2.10.24` - linux; arm variant v7

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

### `nats:2.10.24` - unknown; unknown

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

### `nats:2.10.24` - linux; arm64 variant v8

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
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24` - unknown; unknown

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

### `nats:2.10.24` - linux; ppc64le

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
		Last Modified: Wed, 18 Dec 2024 00:00:47 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2024e9028623ac2d4facbfcc79793de84acf606af93e2a58405c55018f61c3`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24` - unknown; unknown

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

### `nats:2.10.24` - linux; s390x

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
		Last Modified: Wed, 18 Dec 2024 00:00:38 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b0d648957d541b8618bbb5ede323354ca5ffe9aeb3d1dbc9c352ea097e36a2`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24` - unknown; unknown

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

### `nats:2.10.24` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Fri, 13 Dec 2024 15:43:11 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Wed, 18 Dec 2024 00:00:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.24-alpine`

```console
$ docker pull nats@sha256:fd981e2ab99000964bd15286054e61fcc445732fd907db039f260fc0b824b314
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

### `nats:2.10.24-alpine` - linux; amd64

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
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
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

### `nats:2.10.24-alpine` - unknown; unknown

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
		Last Modified: Tue, 14 Jan 2025 20:44:42 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:433eace2afe3116663501e605137b1342e594cacdb6966f39a4d0df268bf1db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9377176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5e4870785bb8d3ce233f8e51d75b3c836d532a4b108a10ec5b904eece338a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf930c71ea8a206b4086d5c226d0bb29b91312f4ba0fb5686ed213131f7c1fce`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 6.0 MB (6012322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3eae10f614d94a7bcc2f8da2f396371afed6fcf19a2a0fa09912e2a8928d16`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac55c9747f66c4223ad92350b9c2f4ae632289aa54c0896ff2c4bfb51fe226c`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e926308a529ca3df71bab310384933d7494a7b9dbd5a1c19897bc8d0ac96d7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9cda5cb22de22806f653121b4f4280e163cfeb76c7bda813be4a23180c799d`

```dockerfile
```

-	Layers:
	-	`sha256:443e6c2877a7f9af9e85b02786a2cd315d99fd6081a70794d949cfa9b32df2d6`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine` - linux; arm variant v7

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

### `nats:2.10.24-alpine` - unknown; unknown

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

### `nats:2.10.24-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:06f83448f3998be4a3663bb016818a5e77a0dabc0b7e4cde4631b7229e9bc051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9908604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d31bd54bf304ebf7853a6da58b3a77e56942fc898c6bee4f3aeac90fe7146db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2319f4b861d20d91a79cb0b31fa138c4fa0f0e8e0f1d48241f67e8057aebae3`  
		Last Modified: Wed, 08 Jan 2025 18:43:13 GMT  
		Size: 5.9 MB (5915276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18be591190612e251286e917fa3eb6f615be7aa9bea5c411422a8e2c94100b9b`  
		Last Modified: Wed, 08 Jan 2025 18:43:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43aededc0983f2e468a526a5a2c0ce30a0094b60a0e5436abf152cac39ad4301`  
		Last Modified: Tue, 14 Jan 2025 20:54:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1e6852827907d03087f78ba2499420258c71c556f679ebee85b527c6d44bfb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c084013fe4a7c0717ee95605f965902e8757de29f4ac5654e97d94b44157b1`

```dockerfile
```

-	Layers:
	-	`sha256:8a790b3bd9ae36824a545f0b1cf838d02166e5d54a3f2fc640990a4c6e839992`  
		Last Modified: Wed, 08 Jan 2025 18:43:12 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:dba35cd86f317f0d4890697bfc5958af2ce36b261fb47d6ee7c6a0b329413e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9456147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6519bc2a29fc7004298799e4cdd113cb764aae1d8b829b72798b48740283cda3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083843bb209f63812a31ab46fe5bcf0253b9604abe5cd0b2f567e6ec9b5c0d1a`  
		Last Modified: Wed, 08 Jan 2025 18:29:05 GMT  
		Size: 5.9 MB (5881578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1278fab8bd865c13254e886eebbdf15b221951118726df5d7ecc1d28c895a590`  
		Last Modified: Wed, 08 Jan 2025 18:29:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6213e9bcfdb590de78a8793596ccd78d7d3e1338c2f0f51dd766df6fccbd920e`  
		Last Modified: Wed, 08 Jan 2025 18:29:04 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:fef206b3ac985104e9f09104765e0ae2a08cf617b2d535be1313154cb37f5639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cdbb6ac4ec6162f10bfeed21eb48f3b7fe5ae64c6faee116ccd9a5931cb690`

```dockerfile
```

-	Layers:
	-	`sha256:e9703e3c1a1be9e27bbc9ae51c1fb1b834ebb3761163483df2853f9a5dbfe36c`  
		Last Modified: Wed, 08 Jan 2025 18:29:04 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine` - linux; s390x

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

### `nats:2.10.24-alpine` - unknown; unknown

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

## `nats:2.10.24-alpine3.21`

```console
$ docker pull nats@sha256:fd981e2ab99000964bd15286054e61fcc445732fd907db039f260fc0b824b314
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

### `nats:2.10.24-alpine3.21` - linux; amd64

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
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
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

### `nats:2.10.24-alpine3.21` - unknown; unknown

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
		Last Modified: Tue, 14 Jan 2025 20:44:42 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:433eace2afe3116663501e605137b1342e594cacdb6966f39a4d0df268bf1db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9377176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5e4870785bb8d3ce233f8e51d75b3c836d532a4b108a10ec5b904eece338a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf930c71ea8a206b4086d5c226d0bb29b91312f4ba0fb5686ed213131f7c1fce`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 6.0 MB (6012322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3eae10f614d94a7bcc2f8da2f396371afed6fcf19a2a0fa09912e2a8928d16`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac55c9747f66c4223ad92350b9c2f4ae632289aa54c0896ff2c4bfb51fe226c`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:e926308a529ca3df71bab310384933d7494a7b9dbd5a1c19897bc8d0ac96d7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9cda5cb22de22806f653121b4f4280e163cfeb76c7bda813be4a23180c799d`

```dockerfile
```

-	Layers:
	-	`sha256:443e6c2877a7f9af9e85b02786a2cd315d99fd6081a70794d949cfa9b32df2d6`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine3.21` - linux; arm variant v7

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

### `nats:2.10.24-alpine3.21` - unknown; unknown

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

### `nats:2.10.24-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:06f83448f3998be4a3663bb016818a5e77a0dabc0b7e4cde4631b7229e9bc051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9908604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d31bd54bf304ebf7853a6da58b3a77e56942fc898c6bee4f3aeac90fe7146db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2319f4b861d20d91a79cb0b31fa138c4fa0f0e8e0f1d48241f67e8057aebae3`  
		Last Modified: Wed, 08 Jan 2025 18:43:13 GMT  
		Size: 5.9 MB (5915276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18be591190612e251286e917fa3eb6f615be7aa9bea5c411422a8e2c94100b9b`  
		Last Modified: Wed, 08 Jan 2025 18:43:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43aededc0983f2e468a526a5a2c0ce30a0094b60a0e5436abf152cac39ad4301`  
		Last Modified: Tue, 14 Jan 2025 20:54:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:1e6852827907d03087f78ba2499420258c71c556f679ebee85b527c6d44bfb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c084013fe4a7c0717ee95605f965902e8757de29f4ac5654e97d94b44157b1`

```dockerfile
```

-	Layers:
	-	`sha256:8a790b3bd9ae36824a545f0b1cf838d02166e5d54a3f2fc640990a4c6e839992`  
		Last Modified: Wed, 08 Jan 2025 18:43:12 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:dba35cd86f317f0d4890697bfc5958af2ce36b261fb47d6ee7c6a0b329413e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9456147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6519bc2a29fc7004298799e4cdd113cb764aae1d8b829b72798b48740283cda3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083843bb209f63812a31ab46fe5bcf0253b9604abe5cd0b2f567e6ec9b5c0d1a`  
		Last Modified: Wed, 08 Jan 2025 18:29:05 GMT  
		Size: 5.9 MB (5881578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1278fab8bd865c13254e886eebbdf15b221951118726df5d7ecc1d28c895a590`  
		Last Modified: Wed, 08 Jan 2025 18:29:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6213e9bcfdb590de78a8793596ccd78d7d3e1338c2f0f51dd766df6fccbd920e`  
		Last Modified: Wed, 08 Jan 2025 18:29:04 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:fef206b3ac985104e9f09104765e0ae2a08cf617b2d535be1313154cb37f5639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cdbb6ac4ec6162f10bfeed21eb48f3b7fe5ae64c6faee116ccd9a5931cb690`

```dockerfile
```

-	Layers:
	-	`sha256:e9703e3c1a1be9e27bbc9ae51c1fb1b834ebb3761163483df2853f9a5dbfe36c`  
		Last Modified: Wed, 08 Jan 2025 18:29:04 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.24-alpine3.21` - linux; s390x

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

### `nats:2.10.24-alpine3.21` - unknown; unknown

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

## `nats:2.10.24-linux`

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

### `nats:2.10.24-linux` - linux; amd64

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

### `nats:2.10.24-linux` - unknown; unknown

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

### `nats:2.10.24-linux` - linux; arm variant v6

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

### `nats:2.10.24-linux` - unknown; unknown

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

### `nats:2.10.24-linux` - linux; arm variant v7

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

### `nats:2.10.24-linux` - unknown; unknown

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

### `nats:2.10.24-linux` - linux; arm64 variant v8

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
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-linux` - unknown; unknown

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

### `nats:2.10.24-linux` - linux; ppc64le

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
		Last Modified: Wed, 18 Dec 2024 00:00:47 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2024e9028623ac2d4facbfcc79793de84acf606af93e2a58405c55018f61c3`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-linux` - unknown; unknown

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

### `nats:2.10.24-linux` - linux; s390x

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
		Last Modified: Wed, 18 Dec 2024 00:00:38 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b0d648957d541b8618bbb5ede323354ca5ffe9aeb3d1dbc9c352ea097e36a2`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-linux` - unknown; unknown

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

## `nats:2.10.24-nanoserver`

```console
$ docker pull nats@sha256:37e1b8a8d0e258480f2b4e3e528c51625f7c66283ec06ca04228db3a08fa024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10.24-nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Fri, 13 Dec 2024 15:43:11 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Wed, 18 Dec 2024 00:00:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.24-nanoserver-1809`

```console
$ docker pull nats@sha256:37e1b8a8d0e258480f2b4e3e528c51625f7c66283ec06ca04228db3a08fa024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10.24-nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Fri, 13 Dec 2024 15:43:11 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Wed, 18 Dec 2024 00:00:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.24-scratch`

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

### `nats:2.10.24-scratch` - linux; amd64

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

### `nats:2.10.24-scratch` - unknown; unknown

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

### `nats:2.10.24-scratch` - linux; arm variant v6

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

### `nats:2.10.24-scratch` - unknown; unknown

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

### `nats:2.10.24-scratch` - linux; arm variant v7

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

### `nats:2.10.24-scratch` - unknown; unknown

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

### `nats:2.10.24-scratch` - linux; arm64 variant v8

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
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-scratch` - unknown; unknown

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

### `nats:2.10.24-scratch` - linux; ppc64le

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
		Last Modified: Wed, 18 Dec 2024 00:00:47 GMT  
		Size: 5.4 MB (5418340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2024e9028623ac2d4facbfcc79793de84acf606af93e2a58405c55018f61c3`  
		Last Modified: Thu, 09 Jan 2025 01:04:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-scratch` - unknown; unknown

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

### `nats:2.10.24-scratch` - linux; s390x

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
		Last Modified: Wed, 18 Dec 2024 00:00:38 GMT  
		Size: 5.7 MB (5748050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b0d648957d541b8618bbb5ede323354ca5ffe9aeb3d1dbc9c352ea097e36a2`  
		Last Modified: Thu, 09 Jan 2025 07:16:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.24-scratch` - unknown; unknown

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

## `nats:2.10.24-windowsservercore`

```console
$ docker pull nats@sha256:358028020ee9c6b6ff8494f70ecbfddddf5b29d36bd20ec1b9b37eb351c46081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10.24-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:c6e3358af2d309d6c2ed2c4321b8d16f0c8c2b817d67b61e77790abeab192882
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64938b4574dd9f4d28b0fdba70a6f3483c75359cd4de6fe307eaf6b4c9e6c5d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 17 Dec 2024 19:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Dec 2024 19:28:54 GMT
ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 19:28:55 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 19:28:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.24/nats-server-v2.10.24-windows-amd64.zip
# Tue, 17 Dec 2024 19:28:57 GMT
ENV NATS_SERVER_SHASUM=bf94c9a9f1685147fd95f6c62f26d16fb72dc8c8c592e2d8c9115e2491c508c3
# Tue, 17 Dec 2024 19:30:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 17 Dec 2024 19:31:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 17 Dec 2024 19:31:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 19:31:06 GMT
EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 19:31:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 19:31:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995e898d38ff13b74b2bf42182403105bd564ca1c8cd3c2bccadac08c8172ca2`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f7d745fbcac3f49a978704fb067848ad5982ff0f7f116bfaceb8e9c68fbc7`  
		Last Modified: Wed, 18 Dec 2024 10:08:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a5927c302d6e5e93a6570c06c06ce9862ef400bd5fea534fea403fd76e9b8`  
		Last Modified: Mon, 06 Jan 2025 17:53:46 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e7b1cd8a1d4aa5917755e9a51eb72256b93ddf6aa3825cbd84213d86f046d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a76e8a87993daefe8a56da532e9ecac69a46fe935f34deac5f3e2ccff312c7`  
		Last Modified: Mon, 06 Jan 2025 19:55:37 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f37de67167c5db5acc1c6ba5c9f86ac4f699f4c646ecae8bccaaa2a6b86bb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:14 GMT  
		Size: 465.9 KB (465852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125faf71663c9c259588da9545dcfc1d961e59d92ce5a9486c7d389cb61bc2c`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 6.4 MB (6375751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9b5ddb5fe65a52ed1c161189ff40d0273af9d50a8a6777a98abffd5b4f7d0`  
		Last Modified: Wed, 18 Dec 2024 00:00:14 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6b8c72206232edf4922cfb68939224b12d0d8eb8e2e4c88e5e66875586d0b`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ec3b766844bacc1ba6a7d126a373851ec2b899f045cddd539bc7f1f7ffbd6`  
		Last Modified: Tue, 07 Jan 2025 03:47:10 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d656e63d77c756e50abf1d5d895ac8c06814dd594cc1bf16ea92894907949e`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.24-windowsservercore-1809`

```console
$ docker pull nats@sha256:358028020ee9c6b6ff8494f70ecbfddddf5b29d36bd20ec1b9b37eb351c46081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10.24-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:c6e3358af2d309d6c2ed2c4321b8d16f0c8c2b817d67b61e77790abeab192882
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64938b4574dd9f4d28b0fdba70a6f3483c75359cd4de6fe307eaf6b4c9e6c5d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 17 Dec 2024 19:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Dec 2024 19:28:54 GMT
ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 19:28:55 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 19:28:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.24/nats-server-v2.10.24-windows-amd64.zip
# Tue, 17 Dec 2024 19:28:57 GMT
ENV NATS_SERVER_SHASUM=bf94c9a9f1685147fd95f6c62f26d16fb72dc8c8c592e2d8c9115e2491c508c3
# Tue, 17 Dec 2024 19:30:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 17 Dec 2024 19:31:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 17 Dec 2024 19:31:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 19:31:06 GMT
EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 19:31:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 19:31:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995e898d38ff13b74b2bf42182403105bd564ca1c8cd3c2bccadac08c8172ca2`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f7d745fbcac3f49a978704fb067848ad5982ff0f7f116bfaceb8e9c68fbc7`  
		Last Modified: Wed, 18 Dec 2024 10:08:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a5927c302d6e5e93a6570c06c06ce9862ef400bd5fea534fea403fd76e9b8`  
		Last Modified: Mon, 06 Jan 2025 17:53:46 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e7b1cd8a1d4aa5917755e9a51eb72256b93ddf6aa3825cbd84213d86f046d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a76e8a87993daefe8a56da532e9ecac69a46fe935f34deac5f3e2ccff312c7`  
		Last Modified: Mon, 06 Jan 2025 19:55:37 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f37de67167c5db5acc1c6ba5c9f86ac4f699f4c646ecae8bccaaa2a6b86bb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:14 GMT  
		Size: 465.9 KB (465852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125faf71663c9c259588da9545dcfc1d961e59d92ce5a9486c7d389cb61bc2c`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 6.4 MB (6375751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9b5ddb5fe65a52ed1c161189ff40d0273af9d50a8a6777a98abffd5b4f7d0`  
		Last Modified: Wed, 18 Dec 2024 00:00:14 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6b8c72206232edf4922cfb68939224b12d0d8eb8e2e4c88e5e66875586d0b`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ec3b766844bacc1ba6a7d126a373851ec2b899f045cddd539bc7f1f7ffbd6`  
		Last Modified: Tue, 07 Jan 2025 03:47:10 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d656e63d77c756e50abf1d5d895ac8c06814dd594cc1bf16ea92894907949e`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:fd981e2ab99000964bd15286054e61fcc445732fd907db039f260fc0b824b314
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
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:44:42 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:433eace2afe3116663501e605137b1342e594cacdb6966f39a4d0df268bf1db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9377176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5e4870785bb8d3ce233f8e51d75b3c836d532a4b108a10ec5b904eece338a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf930c71ea8a206b4086d5c226d0bb29b91312f4ba0fb5686ed213131f7c1fce`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 6.0 MB (6012322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3eae10f614d94a7bcc2f8da2f396371afed6fcf19a2a0fa09912e2a8928d16`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac55c9747f66c4223ad92350b9c2f4ae632289aa54c0896ff2c4bfb51fe226c`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e926308a529ca3df71bab310384933d7494a7b9dbd5a1c19897bc8d0ac96d7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9cda5cb22de22806f653121b4f4280e163cfeb76c7bda813be4a23180c799d`

```dockerfile
```

-	Layers:
	-	`sha256:443e6c2877a7f9af9e85b02786a2cd315d99fd6081a70794d949cfa9b32df2d6`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 14.4 KB (14430 bytes)  
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
$ docker pull nats@sha256:06f83448f3998be4a3663bb016818a5e77a0dabc0b7e4cde4631b7229e9bc051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9908604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d31bd54bf304ebf7853a6da58b3a77e56942fc898c6bee4f3aeac90fe7146db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2319f4b861d20d91a79cb0b31fa138c4fa0f0e8e0f1d48241f67e8057aebae3`  
		Last Modified: Wed, 08 Jan 2025 18:43:13 GMT  
		Size: 5.9 MB (5915276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18be591190612e251286e917fa3eb6f615be7aa9bea5c411422a8e2c94100b9b`  
		Last Modified: Wed, 08 Jan 2025 18:43:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43aededc0983f2e468a526a5a2c0ce30a0094b60a0e5436abf152cac39ad4301`  
		Last Modified: Tue, 14 Jan 2025 20:54:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1e6852827907d03087f78ba2499420258c71c556f679ebee85b527c6d44bfb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c084013fe4a7c0717ee95605f965902e8757de29f4ac5654e97d94b44157b1`

```dockerfile
```

-	Layers:
	-	`sha256:8a790b3bd9ae36824a545f0b1cf838d02166e5d54a3f2fc640990a4c6e839992`  
		Last Modified: Wed, 08 Jan 2025 18:43:12 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:dba35cd86f317f0d4890697bfc5958af2ce36b261fb47d6ee7c6a0b329413e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9456147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6519bc2a29fc7004298799e4cdd113cb764aae1d8b829b72798b48740283cda3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083843bb209f63812a31ab46fe5bcf0253b9604abe5cd0b2f567e6ec9b5c0d1a`  
		Last Modified: Wed, 08 Jan 2025 18:29:05 GMT  
		Size: 5.9 MB (5881578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1278fab8bd865c13254e886eebbdf15b221951118726df5d7ecc1d28c895a590`  
		Last Modified: Wed, 08 Jan 2025 18:29:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6213e9bcfdb590de78a8793596ccd78d7d3e1338c2f0f51dd766df6fccbd920e`  
		Last Modified: Wed, 08 Jan 2025 18:29:04 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:fef206b3ac985104e9f09104765e0ae2a08cf617b2d535be1313154cb37f5639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cdbb6ac4ec6162f10bfeed21eb48f3b7fe5ae64c6faee116ccd9a5931cb690`

```dockerfile
```

-	Layers:
	-	`sha256:e9703e3c1a1be9e27bbc9ae51c1fb1b834ebb3761163483df2853f9a5dbfe36c`  
		Last Modified: Wed, 08 Jan 2025 18:29:04 GMT  
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
$ docker pull nats@sha256:fd981e2ab99000964bd15286054e61fcc445732fd907db039f260fc0b824b314
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
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:44:42 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:433eace2afe3116663501e605137b1342e594cacdb6966f39a4d0df268bf1db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9377176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5e4870785bb8d3ce233f8e51d75b3c836d532a4b108a10ec5b904eece338a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf930c71ea8a206b4086d5c226d0bb29b91312f4ba0fb5686ed213131f7c1fce`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 6.0 MB (6012322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3eae10f614d94a7bcc2f8da2f396371afed6fcf19a2a0fa09912e2a8928d16`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 564.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac55c9747f66c4223ad92350b9c2f4ae632289aa54c0896ff2c4bfb51fe226c`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:e926308a529ca3df71bab310384933d7494a7b9dbd5a1c19897bc8d0ac96d7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9cda5cb22de22806f653121b4f4280e163cfeb76c7bda813be4a23180c799d`

```dockerfile
```

-	Layers:
	-	`sha256:443e6c2877a7f9af9e85b02786a2cd315d99fd6081a70794d949cfa9b32df2d6`  
		Last Modified: Wed, 08 Jan 2025 18:43:33 GMT  
		Size: 14.4 KB (14430 bytes)  
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
$ docker pull nats@sha256:06f83448f3998be4a3663bb016818a5e77a0dabc0b7e4cde4631b7229e9bc051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9908604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d31bd54bf304ebf7853a6da58b3a77e56942fc898c6bee4f3aeac90fe7146db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2319f4b861d20d91a79cb0b31fa138c4fa0f0e8e0f1d48241f67e8057aebae3`  
		Last Modified: Wed, 08 Jan 2025 18:43:13 GMT  
		Size: 5.9 MB (5915276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18be591190612e251286e917fa3eb6f615be7aa9bea5c411422a8e2c94100b9b`  
		Last Modified: Wed, 08 Jan 2025 18:43:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43aededc0983f2e468a526a5a2c0ce30a0094b60a0e5436abf152cac39ad4301`  
		Last Modified: Tue, 14 Jan 2025 20:54:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:1e6852827907d03087f78ba2499420258c71c556f679ebee85b527c6d44bfb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c084013fe4a7c0717ee95605f965902e8757de29f4ac5654e97d94b44157b1`

```dockerfile
```

-	Layers:
	-	`sha256:8a790b3bd9ae36824a545f0b1cf838d02166e5d54a3f2fc640990a4c6e839992`  
		Last Modified: Wed, 08 Jan 2025 18:43:12 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:dba35cd86f317f0d4890697bfc5958af2ce36b261fb47d6ee7c6a0b329413e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9456147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6519bc2a29fc7004298799e4cdd113cb764aae1d8b829b72798b48740283cda3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 17 Dec 2024 17:21:01 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083843bb209f63812a31ab46fe5bcf0253b9604abe5cd0b2f567e6ec9b5c0d1a`  
		Last Modified: Wed, 08 Jan 2025 18:29:05 GMT  
		Size: 5.9 MB (5881578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1278fab8bd865c13254e886eebbdf15b221951118726df5d7ecc1d28c895a590`  
		Last Modified: Wed, 08 Jan 2025 18:29:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6213e9bcfdb590de78a8793596ccd78d7d3e1338c2f0f51dd766df6fccbd920e`  
		Last Modified: Wed, 08 Jan 2025 18:29:04 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:fef206b3ac985104e9f09104765e0ae2a08cf617b2d535be1313154cb37f5639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cdbb6ac4ec6162f10bfeed21eb48f3b7fe5ae64c6faee116ccd9a5931cb690`

```dockerfile
```

-	Layers:
	-	`sha256:e9703e3c1a1be9e27bbc9ae51c1fb1b834ebb3761163483df2853f9a5dbfe36c`  
		Last Modified: Wed, 08 Jan 2025 18:29:04 GMT  
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
$ docker pull nats@sha256:e7fb72b546e897024123450c257a5874d3625a48e17adcb8de234cb202a9cdcc
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
	-	windows version 10.0.17763.6659; amd64

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
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:47 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:38 GMT  
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

### `nats:latest` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Fri, 13 Dec 2024 15:43:11 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Wed, 18 Dec 2024 00:00:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
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
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:47 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:38 GMT  
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
$ docker pull nats@sha256:37e1b8a8d0e258480f2b4e3e528c51625f7c66283ec06ca04228db3a08fa024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Fri, 13 Dec 2024 15:43:11 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Wed, 18 Dec 2024 00:00:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:37e1b8a8d0e258480f2b4e3e528c51625f7c66283ec06ca04228db3a08fa024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:a3bf98913be025c2083ebd5687c133ab5b00f3a1894a3fe2231a87894b64bed0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50684e4ed1bf0d28623bfd52d2bfd9a7c4111c83ceaabd37a09cbf397e675281`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Tue, 17 Dec 2024 20:08:15 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 20:08:18 GMT
RUN cmd /S /C #(nop) COPY file:32d2c78f0dd94e383b45881b640cf1b2c9c27decb4a66e09babbe6a0f796087f in C:\nats-server.exe 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 20:08:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 20:08:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Fri, 13 Dec 2024 15:43:11 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f2ef448a775bed9c6f05668d734eb51754170fdfc93c55c99bbaa763bf0d4e`  
		Last Modified: Tue, 17 Dec 2024 20:08:26 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe350f8421c39c736eb0f8180693ff45eedcd35a224bc510bd2626a0996409b`  
		Last Modified: Tue, 17 Dec 2024 20:08:25 GMT  
		Size: 6.0 MB (6025803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd8a7a90698ba96911ac6344eb5f5dd88c4dfebd29047be607133fadef68165`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f84b1a718e07866b0c5d7f7666c682f746339824f50d2010237f8129d983c34`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be4b8e9d23c6bed197e181271e99e2a123100ad014b841f2409aaa51fe58303`  
		Last Modified: Wed, 18 Dec 2024 00:00:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb4f7ea4c581f0a9e1eb6519dba6818337a039607974ce3fd7131a13ea51b0`  
		Last Modified: Tue, 17 Dec 2024 20:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
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
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:47 GMT  
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
		Last Modified: Wed, 18 Dec 2024 00:00:38 GMT  
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
$ docker pull nats@sha256:358028020ee9c6b6ff8494f70ecbfddddf5b29d36bd20ec1b9b37eb351c46081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:c6e3358af2d309d6c2ed2c4321b8d16f0c8c2b817d67b61e77790abeab192882
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64938b4574dd9f4d28b0fdba70a6f3483c75359cd4de6fe307eaf6b4c9e6c5d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 17 Dec 2024 19:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Dec 2024 19:28:54 GMT
ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 19:28:55 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 19:28:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.24/nats-server-v2.10.24-windows-amd64.zip
# Tue, 17 Dec 2024 19:28:57 GMT
ENV NATS_SERVER_SHASUM=bf94c9a9f1685147fd95f6c62f26d16fb72dc8c8c592e2d8c9115e2491c508c3
# Tue, 17 Dec 2024 19:30:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 17 Dec 2024 19:31:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 17 Dec 2024 19:31:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 19:31:06 GMT
EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 19:31:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 19:31:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995e898d38ff13b74b2bf42182403105bd564ca1c8cd3c2bccadac08c8172ca2`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f7d745fbcac3f49a978704fb067848ad5982ff0f7f116bfaceb8e9c68fbc7`  
		Last Modified: Wed, 18 Dec 2024 10:08:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a5927c302d6e5e93a6570c06c06ce9862ef400bd5fea534fea403fd76e9b8`  
		Last Modified: Mon, 06 Jan 2025 17:53:46 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e7b1cd8a1d4aa5917755e9a51eb72256b93ddf6aa3825cbd84213d86f046d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a76e8a87993daefe8a56da532e9ecac69a46fe935f34deac5f3e2ccff312c7`  
		Last Modified: Mon, 06 Jan 2025 19:55:37 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f37de67167c5db5acc1c6ba5c9f86ac4f699f4c646ecae8bccaaa2a6b86bb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:14 GMT  
		Size: 465.9 KB (465852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125faf71663c9c259588da9545dcfc1d961e59d92ce5a9486c7d389cb61bc2c`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 6.4 MB (6375751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9b5ddb5fe65a52ed1c161189ff40d0273af9d50a8a6777a98abffd5b4f7d0`  
		Last Modified: Wed, 18 Dec 2024 00:00:14 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6b8c72206232edf4922cfb68939224b12d0d8eb8e2e4c88e5e66875586d0b`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ec3b766844bacc1ba6a7d126a373851ec2b899f045cddd539bc7f1f7ffbd6`  
		Last Modified: Tue, 07 Jan 2025 03:47:10 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d656e63d77c756e50abf1d5d895ac8c06814dd594cc1bf16ea92894907949e`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:358028020ee9c6b6ff8494f70ecbfddddf5b29d36bd20ec1b9b37eb351c46081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:c6e3358af2d309d6c2ed2c4321b8d16f0c8c2b817d67b61e77790abeab192882
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64938b4574dd9f4d28b0fdba70a6f3483c75359cd4de6fe307eaf6b4c9e6c5d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 17 Dec 2024 19:28:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Dec 2024 19:28:54 GMT
ENV NATS_DOCKERIZED=1
# Tue, 17 Dec 2024 19:28:55 GMT
ENV NATS_SERVER=2.10.24
# Tue, 17 Dec 2024 19:28:56 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.24/nats-server-v2.10.24-windows-amd64.zip
# Tue, 17 Dec 2024 19:28:57 GMT
ENV NATS_SERVER_SHASUM=bf94c9a9f1685147fd95f6c62f26d16fb72dc8c8c592e2d8c9115e2491c508c3
# Tue, 17 Dec 2024 19:30:38 GMT
RUN Set-PSDebug -Trace 2
# Tue, 17 Dec 2024 19:31:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 17 Dec 2024 19:31:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 17 Dec 2024 19:31:06 GMT
EXPOSE 4222 6222 8222
# Tue, 17 Dec 2024 19:31:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 17 Dec 2024 19:31:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995e898d38ff13b74b2bf42182403105bd564ca1c8cd3c2bccadac08c8172ca2`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f7d745fbcac3f49a978704fb067848ad5982ff0f7f116bfaceb8e9c68fbc7`  
		Last Modified: Wed, 18 Dec 2024 10:08:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a5927c302d6e5e93a6570c06c06ce9862ef400bd5fea534fea403fd76e9b8`  
		Last Modified: Mon, 06 Jan 2025 17:53:46 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e7b1cd8a1d4aa5917755e9a51eb72256b93ddf6aa3825cbd84213d86f046d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a76e8a87993daefe8a56da532e9ecac69a46fe935f34deac5f3e2ccff312c7`  
		Last Modified: Mon, 06 Jan 2025 19:55:37 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f37de67167c5db5acc1c6ba5c9f86ac4f699f4c646ecae8bccaaa2a6b86bb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:14 GMT  
		Size: 465.9 KB (465852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125faf71663c9c259588da9545dcfc1d961e59d92ce5a9486c7d389cb61bc2c`  
		Last Modified: Tue, 17 Dec 2024 19:31:13 GMT  
		Size: 6.4 MB (6375751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f9b5ddb5fe65a52ed1c161189ff40d0273af9d50a8a6777a98abffd5b4f7d0`  
		Last Modified: Wed, 18 Dec 2024 00:00:14 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6b8c72206232edf4922cfb68939224b12d0d8eb8e2e4c88e5e66875586d0b`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ec3b766844bacc1ba6a7d126a373851ec2b899f045cddd539bc7f1f7ffbd6`  
		Last Modified: Tue, 07 Jan 2025 03:47:10 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d656e63d77c756e50abf1d5d895ac8c06814dd594cc1bf16ea92894907949e`  
		Last Modified: Tue, 17 Dec 2024 19:31:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
