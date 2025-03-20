## `nats:latest`

```console
$ docker pull nats@sha256:c2f85f32bf6692d477626ce4c159a54553c8e027b1e01ea26621071fc21fd155
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
	-	windows version 10.0.17763.7009; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:5a071647152d878d8d05477b9d9c4d1b1e1a58f7164057728c8f6d89e9129e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6280540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc9f7936d67f977b2c7e204c4cdcfdf98bc239d2991ad10bd58d68eb4add1e7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 19 Mar 2025 16:37:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 19 Mar 2025 16:37:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 19 Mar 2025 16:37:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 19 Mar 2025 16:37:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 19 Mar 2025 16:37:49 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 19 Mar 2025 16:37:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:819937ed8a4028c3d09b007417009d1dd4a6287e268e55655cabc133cf530f7d`  
		Last Modified: Wed, 19 Mar 2025 16:42:52 GMT  
		Size: 6.3 MB (6280034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f6d65c0c10ba698025259b6928d6f249c6aa897db1ff19a4ddf4f8378fd38`  
		Last Modified: Wed, 19 Mar 2025 21:08:00 GMT  
		Size: 506.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:797f1d4859b1433e0f0a4d733d996802bf44b06270f33bf07b4f56984e388a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112ae24768cdfdf4b5ab9543ee20cabcd76e15bfad9294993e45cd2b961cf938`

```dockerfile
```

-	Layers:
	-	`sha256:e825195c55d10e9783ecbb486c830c06505c50c048d2ea7c04f9106296701214`  
		Last Modified: Wed, 19 Mar 2025 21:08:00 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:50e59da10dc5db01e19fe9c36939335ce64ea5e4bc0eede171fcbab88465dbeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6000424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc3b1fc701946731c1cace85536ce9ed4103b9cb340693d4b8bed6040bb411b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 19 Mar 2025 16:37:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 19 Mar 2025 16:37:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 19 Mar 2025 16:37:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 19 Mar 2025 16:37:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 19 Mar 2025 16:37:49 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 19 Mar 2025 16:37:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:97dc4d7d7c81537e09d55f25c6179a90576ed77e732c6290561e337be4ffa59b`  
		Last Modified: Wed, 19 Mar 2025 16:42:49 GMT  
		Size: 6.0 MB (5999914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf32ab8e05513266b3a4d0b327187b110730be4f3baddfeb75d0586f97e5c97`  
		Last Modified: Wed, 19 Mar 2025 21:07:18 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:b9536b22c685bb355107ddce81dfea545c2f52ede502bd691981eafb785cf7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc05dc7b4e06dc04746870aee16dd4e044a6593f81e529e9e887d6cccfdd645`

```dockerfile
```

-	Layers:
	-	`sha256:33a49d0b1efd62a879e5759a8fbd23186c601003db34ceb9dec809479852b4f4`  
		Last Modified: Wed, 19 Mar 2025 21:07:18 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ba3f53e77bfe68ec915e217e98e27eef3c1dc6582312ecfdff74282af83f27f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5991108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcde9bd1a6e573a6fb19557dfdccad75ea19c144369fc9f1a996b4c094e67e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 19 Mar 2025 16:37:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 19 Mar 2025 16:37:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 19 Mar 2025 16:37:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 19 Mar 2025 16:37:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 19 Mar 2025 16:37:49 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 19 Mar 2025 16:37:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b822286bde36186e2380279ead71279ab7294bf250f55aaf8bf6d4770ae84ce5`  
		Last Modified: Wed, 19 Mar 2025 16:42:51 GMT  
		Size: 6.0 MB (5990600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a38020ffc8a376a117c636de2a0eeb692526c89d67e9677c42aae810fa530d`  
		Last Modified: Wed, 19 Mar 2025 21:07:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:a44410c0dba1a374562a761d12231155886c33def7b6fe607d386625799021bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160af38107e1688ac5695087999bcb3a2da680ab9885c132a2aad8a01d7a2e99`

```dockerfile
```

-	Layers:
	-	`sha256:1484e4c1fa5f08946b20e11d8a3f03be035fa3c57a3c9413acccdd456a13a161`  
		Last Modified: Wed, 19 Mar 2025 21:07:09 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5b39f18a68d525349b8342743703356df26415df7ddb80854343b28659a15367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1621143ad612f99d3ac9a46b461b1dfbbdaf7cb3ad1f0b2b387d9071d79f0ad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 19 Mar 2025 16:37:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 19 Mar 2025 16:37:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 19 Mar 2025 16:37:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 19 Mar 2025 16:37:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 19 Mar 2025 16:37:49 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 19 Mar 2025 16:37:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37f8bea80233611a6393ba9b43e0d5b9487a0e5675862e53cc48c922f0189986`  
		Last Modified: Wed, 19 Mar 2025 16:42:49 GMT  
		Size: 5.8 MB (5775494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1afbd4f0f1a5a28aa16ca864174d0666d154ed2eaf222e29606aa72cddccca1`  
		Last Modified: Wed, 19 Mar 2025 21:57:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:6e8482102e355d0a7d9b8f8184c3bd19c98e57544fe1a79b2db9ab3628f89e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62adb534fedc07f1169dc165a70503ff5da7a9c51e2cadbdbfc03a2f41a798a`

```dockerfile
```

-	Layers:
	-	`sha256:ef5f1dc961aa2787f4175edd0794823fb0c57a526f81ae35e68021d9378b692b`  
		Last Modified: Wed, 19 Mar 2025 21:57:43 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:c68df4ee9c4ef8fe44bed29dfe1fad420aa206ecd1d63298e3cf5006d12c5c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5756930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b70e5bc90a606e80700bc308bdef831324993ad2f64525a4d04b96bf763de12`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 19 Mar 2025 16:37:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 19 Mar 2025 16:37:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 19 Mar 2025 16:37:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 19 Mar 2025 16:37:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 19 Mar 2025 16:37:49 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 19 Mar 2025 16:37:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8ebc7e93ff4428a96def93bc4ed5eaa9df37356631613880900a9e8e7c182ed8`  
		Last Modified: Wed, 19 Mar 2025 16:42:50 GMT  
		Size: 5.8 MB (5756420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8428ee8ec718cdbd462bc888f376931adaa0c39ffcbd7792b12ced9bb5885a`  
		Last Modified: Wed, 19 Mar 2025 21:07:52 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:d668ba47c3e68124e54f296b1cb41517b9b381f44a5e38c0bb326ac76c7f060e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8076807ce209e28b55c0adb8aa4097a5ce710904beffea9cba32037a808dea3`

```dockerfile
```

-	Layers:
	-	`sha256:b84f7930793a2a1995bdfb2fd2c41233f1d27012a77e0468bf20b2ae8d809b6d`  
		Last Modified: Wed, 19 Mar 2025 21:07:51 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:b76e30e8111c3dd844901a7f620548ea5f7e459a785b37cef3a3b8cbaa238a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6121573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fedf13f37ed10d572c130792bb98becc9984b94667d63aefdc5022dfbb20a5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 19 Mar 2025 16:37:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 19 Mar 2025 16:37:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Wed, 19 Mar 2025 16:37:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Wed, 19 Mar 2025 16:37:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 19 Mar 2025 16:37:49 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 19 Mar 2025 16:37:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:01ff6f619f600c7b70f6af4ced98852a91aeb5a4e36ce9aa242f35c136d101ab`  
		Last Modified: Wed, 19 Mar 2025 16:42:51 GMT  
		Size: 6.1 MB (6121064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b20631d1ff7947578611d9db2bb36f02662cfd1843cdbe0e3a9d273ed8ca9a`  
		Last Modified: Wed, 19 Mar 2025 22:10:20 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:197e7904c85477ec7023f1aa56654ac96173c03131d1c516b37898aa193d5381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1195e0cafac900ec66533b9417228003a98af50dff51a14e48a5f980c312dca0`

```dockerfile
```

-	Layers:
	-	`sha256:64e8ef2a68e868e9a8353ea276d8755d9225c7f387585f1c11e0177efbebb916`  
		Last Modified: Wed, 19 Mar 2025 22:10:20 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:cb7ba5453830fa4b1610a981c9ea36d92c9bbd561bb774e3f71d3a0946fb069f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113368849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e64b4fcd6d57238b7d33408c337f54eba590256714f9cc678625d54943e1ef`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 19 Mar 2025 22:07:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 19 Mar 2025 22:07:40 GMT
RUN cmd /S /C #(nop) COPY file:15d682fe943bd0a85193b4305627addb8f063cba56411dc1ccaeb8a61d0564b9 in C:\nats-server.exe 
# Wed, 19 Mar 2025 22:07:40 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 19 Mar 2025 22:07:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 19 Mar 2025 22:07:41 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 19 Mar 2025 22:07:42 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a47df565d44873f952ab7728a5895a6c632119200503a6bae0c17b185dd266f`  
		Last Modified: Wed, 19 Mar 2025 22:07:45 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3e8e98c8fd1b0213d5a733ada9ea5c6b40d408aeb3b91ce797a4e34897e94d`  
		Last Modified: Wed, 19 Mar 2025 22:07:45 GMT  
		Size: 6.5 MB (6455270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8589fea82a112e37ef5362b1ba630677a51f968addc6686b3d41b37e33f10d`  
		Last Modified: Wed, 19 Mar 2025 22:07:44 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a369fb2a070a0597d8a5a11a9654c8621968985d64ea6d65ee9e7bb240e1f2`  
		Last Modified: Wed, 19 Mar 2025 22:07:44 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d125157dbd1f36bf2a074381323b4bc9913e6b14204991a68880ef4deafda1f`  
		Last Modified: Wed, 19 Mar 2025 22:07:44 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dd54f60c51551596518b3c12d1860f0748316e9bb73882e9e527530e5171ef`  
		Last Modified: Wed, 19 Mar 2025 22:07:44 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
