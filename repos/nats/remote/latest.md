## `nats:latest`

```console
$ docker pull nats@sha256:77a161c7d888a1791d5a46b50cd87a2f8466ce40a33cbb51238d227ace01e35a
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
	-	windows version 10.0.20348.4297; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:eaef43a84f52df75799a1c1d9f41294bd5bfd4dd06804c8c16290aa9509baed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6555945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1486c1d15c26cb5857727094c8fa4923f62b2a26acaa51df789e8acf7f52837f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Oct 2025 12:15:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Oct 2025 12:15:17 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Oct 2025 12:15:17 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Oct 2025 12:15:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Oct 2025 12:15:17 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Oct 2025 12:15:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:791ce61bf865582a0f614b6694f7c4c4e75092f596cc85ba303aff14341f81f4`  
		Last Modified: Tue, 14 Oct 2025 12:17:35 GMT  
		Size: 6.6 MB (6555435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e149582979b3a26d700076d6a3836c41a3d5368d280b9aac2527a38792222fc`  
		Last Modified: Tue, 14 Oct 2025 17:10:29 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:e2ecc62ec40698019598d594a8d21c5ac1a4651a1cd16b0068846ede39b75c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11eebde512c1696ab5e77f0a595d51a6e1f2b445850be55b0cf76c42ee4c6bf6`

```dockerfile
```

-	Layers:
	-	`sha256:12719b84e50ea18e4045975f06e80e2af5d8963ae114d4840f3d0e142622507b`  
		Last Modified: Tue, 14 Oct 2025 17:56:29 GMT  
		Size: 10.5 KB (10464 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:779da9fe6b03189178f45592f0cea0c7879489fbe09ab88f946111e97f10c11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6283439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9301b791e139a14e383232913571bdfbd33e0820b9012951be4084f2744829c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Oct 2025 12:15:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Oct 2025 12:15:17 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Oct 2025 12:15:17 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Oct 2025 12:15:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Oct 2025 12:15:17 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Oct 2025 12:15:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9eb91959a3343b9123c831450635085d847dea6c3ecf42aa6590051376d2e71d`  
		Last Modified: Tue, 14 Oct 2025 12:19:12 GMT  
		Size: 6.3 MB (6282929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2e81047b883a52c7771acfd7831403fd5ade3bcba17c8337a22585b330b6b4`  
		Last Modified: Tue, 14 Oct 2025 17:10:11 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:463eb985963549e6bc4331eb31c800215f395b3b8f291ddc662020b47659256e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0125cc14ee388c212cc537baa5dfc55834af56777df5eae8cbf6c55116435dcf`

```dockerfile
```

-	Layers:
	-	`sha256:8909dc2d1097586ea78e0d2c33513d295c11f43e50ba9223347f691fde9023aa`  
		Last Modified: Tue, 14 Oct 2025 17:56:32 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d64757dbdd6d3c80c5296f6045a97bfb87bdd18898cf54f185655127b06c4c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6270523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df101f3011c26c3983886475aaa65925ea7075a6b2923e0b508339b995c6962`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Oct 2025 12:15:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Oct 2025 12:15:17 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Oct 2025 12:15:17 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Oct 2025 12:15:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Oct 2025 12:15:17 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Oct 2025 12:15:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae7be01fca9b773f8b0de7c0a408c04d232c5b46e24373ebfb4a302a0581ece3`  
		Last Modified: Tue, 14 Oct 2025 12:19:12 GMT  
		Size: 6.3 MB (6270013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca083d112fda54b0bfb437f9bd229ae795d7b6018e8fc83b771898a9dbc8f0e`  
		Last Modified: Tue, 14 Oct 2025 17:09:32 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:a16cf5f77eefcda3fcbb0922a7a36833dff040055df3cc7f3ddd9829070b74fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a43d83b1c17c4782b2ba6026be63a96c0975ca23ec1afdb12dac907239b00f2`

```dockerfile
```

-	Layers:
	-	`sha256:c0f8ad13e5b75d80206c0feaec305958a2eb93bbf24f387c5e2fa8c7d6620ee4`  
		Last Modified: Tue, 14 Oct 2025 17:56:36 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e642c0b2b7c45ab83a855075f33b71284372de69d976553c7d836d7aafcba7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5974451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ce00e7314e6953b0927722e84da2c1906d981de7ef9546c96f3bba27a48305`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Oct 2025 12:15:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Oct 2025 12:15:17 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Oct 2025 12:15:17 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Oct 2025 12:15:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Oct 2025 12:15:17 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Oct 2025 12:15:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9b354384e0e40224f035268cfedcc3f95e221dd07655f546e604f8df1d8c85a1`  
		Last Modified: Tue, 14 Oct 2025 12:19:12 GMT  
		Size: 6.0 MB (5973943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b350c9d238c2fb704232d12539699043c48573333e50015c233e16ed8c0f39`  
		Last Modified: Tue, 14 Oct 2025 17:11:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:9586c489c472e110b5c87fba7be276a76efa571bd36a430fcf3ab30cd4c81b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd5709ea4a5834261771a2f674aa64d4620282df39fcc6c0f00660f5932be42`

```dockerfile
```

-	Layers:
	-	`sha256:204bc94bf35eee64ad7fd5e8c3978ab089690294642ef48a23bc05ac8fda33ef`  
		Last Modified: Tue, 14 Oct 2025 17:56:39 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:8fde041b758c83ee4d2c80df93d22aa87132b7057f2c44ae8f41aa8773b2fccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6023329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f27d9353ea7e11726159ada5428e1f81f25704187ddf53ee77bf464cc0d0f6a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Oct 2025 12:15:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Oct 2025 12:15:17 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Oct 2025 12:15:17 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Oct 2025 12:15:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Oct 2025 12:15:17 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Oct 2025 12:15:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8ebf2e56a63cc3b878663c69bcb8656568ac863d3b7bd480f3d8e18113b90922`  
		Last Modified: Tue, 14 Oct 2025 12:17:32 GMT  
		Size: 6.0 MB (6022819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d66cd874019e03f50ee3bb8a12d4055873586ad5aea7de9cba266d59bb09c7`  
		Last Modified: Tue, 14 Oct 2025 17:10:22 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:83abef78317fb2b6ce6864b0e831f94a8ce55424150638c4290903bbd3effa15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43ffbaee08f927c763c8af8401796a02f408ec9db4c9e6bad087b75bd2fffe4`

```dockerfile
```

-	Layers:
	-	`sha256:7b67088b3de68776d65425cc928dc7cf059e239b7ccc606192b1aaf1dda55802`  
		Last Modified: Tue, 14 Oct 2025 17:56:43 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:e0cbdcb96a49a080d9180a2dc76ba75d8dc09345d5be140c1d584b9c013171f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6398297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0e08f5393940cb798f6aa9eec4dbe8f06036ab737caf73aee341db6b136472`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Oct 2025 12:15:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Oct 2025 12:15:17 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Oct 2025 12:15:17 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Oct 2025 12:15:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Oct 2025 12:15:17 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Oct 2025 12:15:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2ed0cb65194d68dcf12ddecd60b6e807ccdec9043cd6f2ee5ddb202397eb7045`  
		Last Modified: Tue, 14 Oct 2025 12:19:11 GMT  
		Size: 6.4 MB (6397787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e149582979b3a26d700076d6a3836c41a3d5368d280b9aac2527a38792222fc`  
		Last Modified: Tue, 14 Oct 2025 17:10:29 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:f4b771c001fecb092b7ab1b160e8ef1b99ffa0240b53d5f29d6fd54353135c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a772ec262dfeb8203b3a4c9651fceb6ba409006578e6df7c6ecc3dd955023de5`

```dockerfile
```

-	Layers:
	-	`sha256:1d8d7cea609ab328ed519712f09e33721ea30ef7cf588c71dc0ed303adeedcb0`  
		Last Modified: Tue, 14 Oct 2025 17:56:47 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.20348.4297; amd64

```console
$ docker pull nats@sha256:0d2cf6213e1e01640a5df39bc43f3aea42f24845bf7137f0bb23ac0794692e70
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129425031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589502f75e52dd2cc5b876b8cf855e520cf78c7289d44d13cad089887d26fc8b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:15:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 24 Oct 2025 19:15:45 GMT
RUN cmd /S /C #(nop) COPY file:686e92130a21a0cff4a93b886b2e653659a4511975aa0c795cb937f76795c7fa in C:\nats-server.exe 
# Fri, 24 Oct 2025 19:15:46 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Fri, 24 Oct 2025 19:15:47 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 24 Oct 2025 19:15:48 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 24 Oct 2025 19:15:49 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10149e5041dcf6df9318e15be2e2d485390cd33f3ec4956fd124cf22a63bc4b5`  
		Last Modified: Fri, 24 Oct 2025 19:16:44 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48ea241e012d48c8b26ea3f8f6e402a9a93424217e86977c139112e4a9aa2ba`  
		Last Modified: Fri, 24 Oct 2025 19:16:45 GMT  
		Size: 6.7 MB (6734972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97e31a63c7d608f9ef5b510ff2d0ec75c12aafc21bc8b9e814f41d43bfd093d`  
		Last Modified: Fri, 24 Oct 2025 19:16:44 GMT  
		Size: 1.7 KB (1699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e71b45fb29670cba7c651d8c5f2bdb91263df015352f9153fdc1b344771fd38`  
		Last Modified: Fri, 24 Oct 2025 19:16:44 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7450af0e1255e37ac5527b52c9111fbb638f71dd37efae865ed2b119b2d75adf`  
		Last Modified: Fri, 24 Oct 2025 19:16:44 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5641622de7c6b823b9a3804b8fdaa6969911572e2f5c047eb4410e7098696ac`  
		Last Modified: Fri, 24 Oct 2025 19:16:44 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
