<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `notary`

-	[`notary:server`](#notaryserver)
-	[`notary:server-0.7.0`](#notaryserver-070)
-	[`notary:signer`](#notarysigner)
-	[`notary:signer-0.7.0`](#notarysigner-070)

## `notary:server`

```console
$ docker pull notary@sha256:755d3a2a71c50534f27f5f4fda3855ae9ff181abe7b8be468c1621e127cb1e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:server` - linux; amd64

```console
$ docker pull notary@sha256:d0245f995d2b0f0b48a6534dfcc01d69a8e8b40cc2afefa12c5debec8821b4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7952164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe35c0f534856452f5db1c237c65a3016f8ab494aae09b01f9db993db0257fc`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:38:02 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 06:38:02 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 12 Nov 2022 06:38:02 GMT
ENV INSTALLDIR=/notary/server
# Sat, 12 Nov 2022 06:38:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 12 Nov 2022 06:38:02 GMT
WORKDIR /notary/server
# Sat, 12 Nov 2022 06:38:03 GMT
COPY /notary-server ./ # buildkit
# Sat, 12 Nov 2022 06:38:03 GMT
RUN ./notary-server --version # buildkit
# Sat, 12 Nov 2022 06:38:03 GMT
COPY ./server-config.json . # buildkit
# Sat, 12 Nov 2022 06:38:03 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 06:38:03 GMT
USER notary
# Sat, 12 Nov 2022 06:38:03 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 06:38:03 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab556644ad7457163fa974396862be0db6a3e9b2a288041b04e6009ae65f4ed`  
		Last Modified: Sat, 12 Nov 2022 06:38:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed42602a65127618c555766dddb85795b2a28b21875015cc78f009e503b964d`  
		Last Modified: Sat, 12 Nov 2022 06:38:18 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f606037229cf543b09e272baae69721fc189abc368dca06db5e4473a7e18043`  
		Last Modified: Sat, 12 Nov 2022 06:38:19 GMT  
		Size: 5.1 MB (5143669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205aa520d53238dab179ef891292c136a1388cfe2c4bf83b3082a29797343796`  
		Last Modified: Sat, 12 Nov 2022 06:38:18 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd9af75aefb91a11fadef9e3b3d32437718ad6e38c664f931e70160e465d644`  
		Last Modified: Sat, 12 Nov 2022 06:38:18 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d72f91b6502eaed3dc0944f2f18bbfa2976f4179e3c9ebc48a2c0087499d12`  
		Last Modified: Sat, 12 Nov 2022 06:38:18 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm variant v6

```console
$ docker pull notary@sha256:b1009bcad7b6a49141436b4fd03fd73ae2b58547f836123cf4b4fd0d0aedbb1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ecccd1c21b9543ad2c0070218ddb0a2bf3d250d3d0daa529a10a5e5f9cce54`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:53:33 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 04:53:33 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 12 Nov 2022 04:53:33 GMT
ENV INSTALLDIR=/notary/server
# Sat, 12 Nov 2022 04:53:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 12 Nov 2022 04:53:33 GMT
WORKDIR /notary/server
# Sat, 12 Nov 2022 04:53:33 GMT
COPY /notary-server ./ # buildkit
# Sat, 12 Nov 2022 04:53:34 GMT
RUN ./notary-server --version # buildkit
# Sat, 12 Nov 2022 04:53:34 GMT
COPY ./server-config.json . # buildkit
# Sat, 12 Nov 2022 04:53:34 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 04:53:34 GMT
USER notary
# Sat, 12 Nov 2022 04:53:34 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 04:53:34 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962f84bc6be5fe2d32e4441665bf4590588a5e805f0f4dc59ca7f20062278a1a`  
		Last Modified: Sat, 12 Nov 2022 04:54:08 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33090c22b1906904caf40830c2082f01799849efbaa3e099979f076f82c8b3a1`  
		Last Modified: Sat, 12 Nov 2022 04:54:05 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed154327c2b3fef4d2bffce7f73433261c0a377fa17a1894062da96a6b1c36d`  
		Last Modified: Sat, 12 Nov 2022 04:54:06 GMT  
		Size: 4.9 MB (4888299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02819c04fd0508bf8e160948a57a10a5e758f72a8276bbbf42857938abdaa892`  
		Last Modified: Sat, 12 Nov 2022 04:54:06 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c16e7a5248dd730be74bd565dadef6ea56f1ae328ce05cc366f6e827eb4cb99`  
		Last Modified: Sat, 12 Nov 2022 04:54:05 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1114f4089f5920f6f3aa6d9e0913d4683ba9225dcdf9723c48fcd1346a744a6`  
		Last Modified: Sat, 12 Nov 2022 04:54:05 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:3e1ec7d20889f7c37f6c13476a2763bb3d5eab5be137e327d7266fb172637566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cada7634040dfd4c2fb6ec3b7ab4b20c831addd6233a912373688a70cdef2e17`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:36:49 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 04:36:49 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 12 Nov 2022 04:36:49 GMT
ENV INSTALLDIR=/notary/server
# Sat, 12 Nov 2022 04:36:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 12 Nov 2022 04:36:49 GMT
WORKDIR /notary/server
# Sat, 12 Nov 2022 04:36:49 GMT
COPY /notary-server ./ # buildkit
# Sat, 12 Nov 2022 04:36:49 GMT
RUN ./notary-server --version # buildkit
# Sat, 12 Nov 2022 04:36:49 GMT
COPY ./server-config.json . # buildkit
# Sat, 12 Nov 2022 04:36:49 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 04:36:49 GMT
USER notary
# Sat, 12 Nov 2022 04:36:49 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 04:36:49 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d302558fe89c8fe780469f0b8d23bc5062a020060a765fb3f2fbf0d7504a640`  
		Last Modified: Sat, 12 Nov 2022 04:37:07 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e2765c49d0f6fd3ccbc844595f80ded29859b5546f880e4c2a30817ec85cf3`  
		Last Modified: Sat, 12 Nov 2022 04:37:05 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ab16aa9d289192b939cf8bc6a258048be4b1b14a5bac7450d1ccb992a88493`  
		Last Modified: Sat, 12 Nov 2022 04:37:06 GMT  
		Size: 4.7 MB (4731486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8d0df93b3fce10e0eeac63d0e744daa330473f98746261aa8ac8dab31e2889`  
		Last Modified: Sat, 12 Nov 2022 04:37:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c37043c32ac4de9b32a8b409ed6dec9dc27ac9b83c95193a93f4bf2b3322ad`  
		Last Modified: Sat, 12 Nov 2022 04:37:05 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ebc35692711619a05d7ea3c0f41a7fec4ff661d473346460a7ec518c653b02`  
		Last Modified: Sat, 12 Nov 2022 04:37:05 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; 386

```console
$ docker pull notary@sha256:d780e4be9f754930f0eb738679598443d886370a29f8f6208a219df31eb9bb60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7754936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082d2270d0f97c88938354b91761b56cad3a983be86702c85f0d686c859d2589`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:57:54 GMT
RUN adduser -D -H -g "" notary
# Sat, 12 Nov 2022 04:57:55 GMT
EXPOSE 4443
# Sat, 12 Nov 2022 04:57:56 GMT
ENV INSTALLDIR=/notary/server
# Sat, 12 Nov 2022 04:57:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 12 Nov 2022 04:57:58 GMT
WORKDIR /notary/server
# Tue, 15 Nov 2022 23:10:40 GMT
COPY file:ad1246f03eccfc8c7e0395a67eb0dff4aacb2adee1de94c20996385566fbadaa in ./ 
# Tue, 15 Nov 2022 23:10:40 GMT
RUN ./notary-server --version
# Tue, 15 Nov 2022 23:10:42 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Tue, 15 Nov 2022 23:10:43 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Tue, 15 Nov 2022 23:10:43 GMT
USER notary
# Tue, 15 Nov 2022 23:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 15 Nov 2022 23:10:45 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e2a37344f15c9c47f28fb76d0bbfae6f9adb65b4d686216a9a5881505ed0ec`  
		Last Modified: Sat, 12 Nov 2022 04:58:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9866a73f72dbc8d55f6da18666277753336525decc6cf3f5862f64f9aede0bb4`  
		Last Modified: Sat, 12 Nov 2022 04:58:40 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc9004d2f5c95ce63fb41d8e7e9f332ecb95d63a72870409521405d42f6566d`  
		Last Modified: Tue, 15 Nov 2022 23:11:14 GMT  
		Size: 4.9 MB (4944480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6df7a1bda3af2924828c9ad15a461076eb599c1bcc83c22232a6bff5767717`  
		Last Modified: Tue, 15 Nov 2022 23:11:14 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c54feb18d0bfa1c20f849987183f762268d9ffc044aaf2b756efcffb91736e`  
		Last Modified: Tue, 15 Nov 2022 23:11:14 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; ppc64le

```console
$ docker pull notary@sha256:e6a8ac9b060d24f62f33f1770f8e416720a72c829e471bd004c2ab474352ee48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7436994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72375853597e7859b23331c5501aade1ac845dd6e0f06bff7dddadaf68604c2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:12:27 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 07:12:27 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 12 Nov 2022 07:12:27 GMT
ENV INSTALLDIR=/notary/server
# Sat, 12 Nov 2022 07:12:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 12 Nov 2022 07:12:27 GMT
WORKDIR /notary/server
# Sat, 12 Nov 2022 07:12:28 GMT
COPY /notary-server ./ # buildkit
# Sat, 12 Nov 2022 07:12:29 GMT
RUN ./notary-server --version # buildkit
# Sat, 12 Nov 2022 07:12:29 GMT
COPY ./server-config.json . # buildkit
# Sat, 12 Nov 2022 07:12:29 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 07:12:29 GMT
USER notary
# Sat, 12 Nov 2022 07:12:29 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 07:12:29 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15023fe5082ace3d77a3ca4c98a9b31b5bef60a4835bddce618606ee9f17cf6`  
		Last Modified: Sat, 12 Nov 2022 07:13:02 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f15b402da893576104d72bedce0b38fd79217c0335b5c4ce1a6076cebbb1b8a`  
		Last Modified: Sat, 12 Nov 2022 07:12:59 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03950c1bc8dfea7021db47478f14c62bb8f18e10a0c309b093669c3fe3cf3a4`  
		Last Modified: Sat, 12 Nov 2022 07:13:01 GMT  
		Size: 4.6 MB (4633221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdf3e3f4ba8d7c7a7140a57fde58d7bf43d6f366e805be9db623fc4f5863776`  
		Last Modified: Sat, 12 Nov 2022 07:12:59 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e954c091668a5ec48014b3dce35faecfe5d4e56a37397e3a3fee0e3314badc`  
		Last Modified: Sat, 12 Nov 2022 07:12:59 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b3ecad580d4aa95d678b89cf86fb274fe07c8034582e1a74f58151903aa770`  
		Last Modified: Sat, 12 Nov 2022 07:12:59 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; s390x

```console
$ docker pull notary@sha256:870f4bca386cf3b2cace6eb81b7fdf7a41cf612b49d78ab8b4faf3aec65b100e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7562067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc61ec13e1c56504cad297107ee38033a27ecaef5ae0e3e0472301df9022760`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:42:05 GMT
ADD file:b78ae95cbacd853e398f187adaf3be51d9e301a66de8f7a4b6c60a9733075cb5 in / 
# Sat, 12 Nov 2022 03:42:06 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:29:11 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 05:29:11 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 12 Nov 2022 05:29:11 GMT
ENV INSTALLDIR=/notary/server
# Sat, 12 Nov 2022 05:29:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 12 Nov 2022 05:29:11 GMT
WORKDIR /notary/server
# Sat, 12 Nov 2022 05:29:11 GMT
COPY /notary-server ./ # buildkit
# Sat, 12 Nov 2022 05:29:11 GMT
RUN ./notary-server --version # buildkit
# Sat, 12 Nov 2022 05:29:11 GMT
COPY ./server-config.json . # buildkit
# Sat, 12 Nov 2022 05:29:12 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 05:29:12 GMT
USER notary
# Sat, 12 Nov 2022 05:29:12 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 05:29:12 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:cff16a5ffe2df97bc1d10b021c5ceb98bdb36a18a1d70395590444ac204a9b2b`  
		Last Modified: Sat, 12 Nov 2022 03:43:06 GMT  
		Size: 2.6 MB (2591126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4ef31691b8350e3f169efda08440ffc8f858999b921631575acdfd35d88225`  
		Last Modified: Sat, 12 Nov 2022 05:29:49 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba78ca725314efb5b67eb6424fd58fc99193e2ba05a043a971a5d7bb549454fa`  
		Last Modified: Sat, 12 Nov 2022 05:29:47 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c18aee86310db355099abac8db72c7a7ce9cec9d90cd152014bac4c9e362f95`  
		Last Modified: Sat, 12 Nov 2022 05:29:48 GMT  
		Size: 5.0 MB (4968727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d688cb67bac28c4f2f131814b1956c43122b8faa02944a2293a819cf3a62e663`  
		Last Modified: Sat, 12 Nov 2022 05:29:47 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e612ec147d0337956004207865cd1454109cda75072884a75172edbc7aa83af7`  
		Last Modified: Sat, 12 Nov 2022 05:29:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1168634fb4594bf745b436f3a089f254870cdb538142ef25b85c8195e5417533`  
		Last Modified: Sat, 12 Nov 2022 05:29:47 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:server-0.7.0`

```console
$ docker pull notary@sha256:755d3a2a71c50534f27f5f4fda3855ae9ff181abe7b8be468c1621e127cb1e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:server-0.7.0` - linux; amd64

```console
$ docker pull notary@sha256:d0245f995d2b0f0b48a6534dfcc01d69a8e8b40cc2afefa12c5debec8821b4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7952164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe35c0f534856452f5db1c237c65a3016f8ab494aae09b01f9db993db0257fc`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:38:02 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 06:38:02 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 12 Nov 2022 06:38:02 GMT
ENV INSTALLDIR=/notary/server
# Sat, 12 Nov 2022 06:38:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 12 Nov 2022 06:38:02 GMT
WORKDIR /notary/server
# Sat, 12 Nov 2022 06:38:03 GMT
COPY /notary-server ./ # buildkit
# Sat, 12 Nov 2022 06:38:03 GMT
RUN ./notary-server --version # buildkit
# Sat, 12 Nov 2022 06:38:03 GMT
COPY ./server-config.json . # buildkit
# Sat, 12 Nov 2022 06:38:03 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 06:38:03 GMT
USER notary
# Sat, 12 Nov 2022 06:38:03 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 06:38:03 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab556644ad7457163fa974396862be0db6a3e9b2a288041b04e6009ae65f4ed`  
		Last Modified: Sat, 12 Nov 2022 06:38:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed42602a65127618c555766dddb85795b2a28b21875015cc78f009e503b964d`  
		Last Modified: Sat, 12 Nov 2022 06:38:18 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f606037229cf543b09e272baae69721fc189abc368dca06db5e4473a7e18043`  
		Last Modified: Sat, 12 Nov 2022 06:38:19 GMT  
		Size: 5.1 MB (5143669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205aa520d53238dab179ef891292c136a1388cfe2c4bf83b3082a29797343796`  
		Last Modified: Sat, 12 Nov 2022 06:38:18 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd9af75aefb91a11fadef9e3b3d32437718ad6e38c664f931e70160e465d644`  
		Last Modified: Sat, 12 Nov 2022 06:38:18 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d72f91b6502eaed3dc0944f2f18bbfa2976f4179e3c9ebc48a2c0087499d12`  
		Last Modified: Sat, 12 Nov 2022 06:38:18 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:b1009bcad7b6a49141436b4fd03fd73ae2b58547f836123cf4b4fd0d0aedbb1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ecccd1c21b9543ad2c0070218ddb0a2bf3d250d3d0daa529a10a5e5f9cce54`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:53:33 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 04:53:33 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 12 Nov 2022 04:53:33 GMT
ENV INSTALLDIR=/notary/server
# Sat, 12 Nov 2022 04:53:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 12 Nov 2022 04:53:33 GMT
WORKDIR /notary/server
# Sat, 12 Nov 2022 04:53:33 GMT
COPY /notary-server ./ # buildkit
# Sat, 12 Nov 2022 04:53:34 GMT
RUN ./notary-server --version # buildkit
# Sat, 12 Nov 2022 04:53:34 GMT
COPY ./server-config.json . # buildkit
# Sat, 12 Nov 2022 04:53:34 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 04:53:34 GMT
USER notary
# Sat, 12 Nov 2022 04:53:34 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 04:53:34 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962f84bc6be5fe2d32e4441665bf4590588a5e805f0f4dc59ca7f20062278a1a`  
		Last Modified: Sat, 12 Nov 2022 04:54:08 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33090c22b1906904caf40830c2082f01799849efbaa3e099979f076f82c8b3a1`  
		Last Modified: Sat, 12 Nov 2022 04:54:05 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed154327c2b3fef4d2bffce7f73433261c0a377fa17a1894062da96a6b1c36d`  
		Last Modified: Sat, 12 Nov 2022 04:54:06 GMT  
		Size: 4.9 MB (4888299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02819c04fd0508bf8e160948a57a10a5e758f72a8276bbbf42857938abdaa892`  
		Last Modified: Sat, 12 Nov 2022 04:54:06 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c16e7a5248dd730be74bd565dadef6ea56f1ae328ce05cc366f6e827eb4cb99`  
		Last Modified: Sat, 12 Nov 2022 04:54:05 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1114f4089f5920f6f3aa6d9e0913d4683ba9225dcdf9723c48fcd1346a744a6`  
		Last Modified: Sat, 12 Nov 2022 04:54:05 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:3e1ec7d20889f7c37f6c13476a2763bb3d5eab5be137e327d7266fb172637566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cada7634040dfd4c2fb6ec3b7ab4b20c831addd6233a912373688a70cdef2e17`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:36:49 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 04:36:49 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 12 Nov 2022 04:36:49 GMT
ENV INSTALLDIR=/notary/server
# Sat, 12 Nov 2022 04:36:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 12 Nov 2022 04:36:49 GMT
WORKDIR /notary/server
# Sat, 12 Nov 2022 04:36:49 GMT
COPY /notary-server ./ # buildkit
# Sat, 12 Nov 2022 04:36:49 GMT
RUN ./notary-server --version # buildkit
# Sat, 12 Nov 2022 04:36:49 GMT
COPY ./server-config.json . # buildkit
# Sat, 12 Nov 2022 04:36:49 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 04:36:49 GMT
USER notary
# Sat, 12 Nov 2022 04:36:49 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 04:36:49 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d302558fe89c8fe780469f0b8d23bc5062a020060a765fb3f2fbf0d7504a640`  
		Last Modified: Sat, 12 Nov 2022 04:37:07 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e2765c49d0f6fd3ccbc844595f80ded29859b5546f880e4c2a30817ec85cf3`  
		Last Modified: Sat, 12 Nov 2022 04:37:05 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ab16aa9d289192b939cf8bc6a258048be4b1b14a5bac7450d1ccb992a88493`  
		Last Modified: Sat, 12 Nov 2022 04:37:06 GMT  
		Size: 4.7 MB (4731486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8d0df93b3fce10e0eeac63d0e744daa330473f98746261aa8ac8dab31e2889`  
		Last Modified: Sat, 12 Nov 2022 04:37:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c37043c32ac4de9b32a8b409ed6dec9dc27ac9b83c95193a93f4bf2b3322ad`  
		Last Modified: Sat, 12 Nov 2022 04:37:05 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ebc35692711619a05d7ea3c0f41a7fec4ff661d473346460a7ec518c653b02`  
		Last Modified: Sat, 12 Nov 2022 04:37:05 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:d780e4be9f754930f0eb738679598443d886370a29f8f6208a219df31eb9bb60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7754936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082d2270d0f97c88938354b91761b56cad3a983be86702c85f0d686c859d2589`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:57:54 GMT
RUN adduser -D -H -g "" notary
# Sat, 12 Nov 2022 04:57:55 GMT
EXPOSE 4443
# Sat, 12 Nov 2022 04:57:56 GMT
ENV INSTALLDIR=/notary/server
# Sat, 12 Nov 2022 04:57:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 12 Nov 2022 04:57:58 GMT
WORKDIR /notary/server
# Tue, 15 Nov 2022 23:10:40 GMT
COPY file:ad1246f03eccfc8c7e0395a67eb0dff4aacb2adee1de94c20996385566fbadaa in ./ 
# Tue, 15 Nov 2022 23:10:40 GMT
RUN ./notary-server --version
# Tue, 15 Nov 2022 23:10:42 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Tue, 15 Nov 2022 23:10:43 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Tue, 15 Nov 2022 23:10:43 GMT
USER notary
# Tue, 15 Nov 2022 23:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 15 Nov 2022 23:10:45 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e2a37344f15c9c47f28fb76d0bbfae6f9adb65b4d686216a9a5881505ed0ec`  
		Last Modified: Sat, 12 Nov 2022 04:58:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9866a73f72dbc8d55f6da18666277753336525decc6cf3f5862f64f9aede0bb4`  
		Last Modified: Sat, 12 Nov 2022 04:58:40 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc9004d2f5c95ce63fb41d8e7e9f332ecb95d63a72870409521405d42f6566d`  
		Last Modified: Tue, 15 Nov 2022 23:11:14 GMT  
		Size: 4.9 MB (4944480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6df7a1bda3af2924828c9ad15a461076eb599c1bcc83c22232a6bff5767717`  
		Last Modified: Tue, 15 Nov 2022 23:11:14 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c54feb18d0bfa1c20f849987183f762268d9ffc044aaf2b756efcffb91736e`  
		Last Modified: Tue, 15 Nov 2022 23:11:14 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:e6a8ac9b060d24f62f33f1770f8e416720a72c829e471bd004c2ab474352ee48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7436994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72375853597e7859b23331c5501aade1ac845dd6e0f06bff7dddadaf68604c2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:12:27 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 07:12:27 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 12 Nov 2022 07:12:27 GMT
ENV INSTALLDIR=/notary/server
# Sat, 12 Nov 2022 07:12:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 12 Nov 2022 07:12:27 GMT
WORKDIR /notary/server
# Sat, 12 Nov 2022 07:12:28 GMT
COPY /notary-server ./ # buildkit
# Sat, 12 Nov 2022 07:12:29 GMT
RUN ./notary-server --version # buildkit
# Sat, 12 Nov 2022 07:12:29 GMT
COPY ./server-config.json . # buildkit
# Sat, 12 Nov 2022 07:12:29 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 07:12:29 GMT
USER notary
# Sat, 12 Nov 2022 07:12:29 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 07:12:29 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15023fe5082ace3d77a3ca4c98a9b31b5bef60a4835bddce618606ee9f17cf6`  
		Last Modified: Sat, 12 Nov 2022 07:13:02 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f15b402da893576104d72bedce0b38fd79217c0335b5c4ce1a6076cebbb1b8a`  
		Last Modified: Sat, 12 Nov 2022 07:12:59 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03950c1bc8dfea7021db47478f14c62bb8f18e10a0c309b093669c3fe3cf3a4`  
		Last Modified: Sat, 12 Nov 2022 07:13:01 GMT  
		Size: 4.6 MB (4633221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdf3e3f4ba8d7c7a7140a57fde58d7bf43d6f366e805be9db623fc4f5863776`  
		Last Modified: Sat, 12 Nov 2022 07:12:59 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e954c091668a5ec48014b3dce35faecfe5d4e56a37397e3a3fee0e3314badc`  
		Last Modified: Sat, 12 Nov 2022 07:12:59 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b3ecad580d4aa95d678b89cf86fb274fe07c8034582e1a74f58151903aa770`  
		Last Modified: Sat, 12 Nov 2022 07:12:59 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:870f4bca386cf3b2cace6eb81b7fdf7a41cf612b49d78ab8b4faf3aec65b100e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7562067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc61ec13e1c56504cad297107ee38033a27ecaef5ae0e3e0472301df9022760`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:42:05 GMT
ADD file:b78ae95cbacd853e398f187adaf3be51d9e301a66de8f7a4b6c60a9733075cb5 in / 
# Sat, 12 Nov 2022 03:42:06 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:29:11 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 05:29:11 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 12 Nov 2022 05:29:11 GMT
ENV INSTALLDIR=/notary/server
# Sat, 12 Nov 2022 05:29:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 12 Nov 2022 05:29:11 GMT
WORKDIR /notary/server
# Sat, 12 Nov 2022 05:29:11 GMT
COPY /notary-server ./ # buildkit
# Sat, 12 Nov 2022 05:29:11 GMT
RUN ./notary-server --version # buildkit
# Sat, 12 Nov 2022 05:29:11 GMT
COPY ./server-config.json . # buildkit
# Sat, 12 Nov 2022 05:29:12 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 05:29:12 GMT
USER notary
# Sat, 12 Nov 2022 05:29:12 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 05:29:12 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:cff16a5ffe2df97bc1d10b021c5ceb98bdb36a18a1d70395590444ac204a9b2b`  
		Last Modified: Sat, 12 Nov 2022 03:43:06 GMT  
		Size: 2.6 MB (2591126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4ef31691b8350e3f169efda08440ffc8f858999b921631575acdfd35d88225`  
		Last Modified: Sat, 12 Nov 2022 05:29:49 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba78ca725314efb5b67eb6424fd58fc99193e2ba05a043a971a5d7bb549454fa`  
		Last Modified: Sat, 12 Nov 2022 05:29:47 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c18aee86310db355099abac8db72c7a7ce9cec9d90cd152014bac4c9e362f95`  
		Last Modified: Sat, 12 Nov 2022 05:29:48 GMT  
		Size: 5.0 MB (4968727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d688cb67bac28c4f2f131814b1956c43122b8faa02944a2293a819cf3a62e663`  
		Last Modified: Sat, 12 Nov 2022 05:29:47 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e612ec147d0337956004207865cd1454109cda75072884a75172edbc7aa83af7`  
		Last Modified: Sat, 12 Nov 2022 05:29:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1168634fb4594bf745b436f3a089f254870cdb538142ef25b85c8195e5417533`  
		Last Modified: Sat, 12 Nov 2022 05:29:47 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:signer`

```console
$ docker pull notary@sha256:bb75b00e2ad22777b0073e0e29ae8a21d45e0ce4fbe535b4d95313a6280b4267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:signer` - linux; amd64

```console
$ docker pull notary@sha256:55cade7712a7a99cd80e60f3cacc1a51ed29da4d6597d66c08313a70dbb9c8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7565226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0c93846d65121b8323f16ef2806bbecec97aabef96a991262f99a0b1be473a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:38:02 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 06:38:08 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 12 Nov 2022 06:38:08 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 12 Nov 2022 06:38:08 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 06:38:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 06:38:08 GMT
WORKDIR /notary/signer
# Sat, 12 Nov 2022 06:38:08 GMT
COPY /notary-signer ./ # buildkit
# Sat, 12 Nov 2022 06:38:08 GMT
RUN ./notary-signer --version # buildkit
# Sat, 12 Nov 2022 06:38:08 GMT
COPY ./signer-config.json . # buildkit
# Sat, 12 Nov 2022 06:38:08 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 06:38:08 GMT
USER notary
# Sat, 12 Nov 2022 06:38:08 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 06:38:08 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab556644ad7457163fa974396862be0db6a3e9b2a288041b04e6009ae65f4ed`  
		Last Modified: Sat, 12 Nov 2022 06:38:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da59cda2c120691b5be31fdc1571f10856ae5c4527c577ae2f76cd70fcd4a05`  
		Last Modified: Sat, 12 Nov 2022 06:38:29 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c81e7e77b856a4b227f55f4c046dd4a3552e7f3e26f324115728eedf3fddd4`  
		Last Modified: Sat, 12 Nov 2022 06:38:30 GMT  
		Size: 4.8 MB (4756800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cc590c46cc2073e2d2ad5b086f723684d1fec0b2a793fda8366aa6af523b16`  
		Last Modified: Sat, 12 Nov 2022 06:38:29 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c48c354c6b48571de1465f8c01053e9a2eb9a38d245a863094ad3cdd6bd141`  
		Last Modified: Sat, 12 Nov 2022 06:38:29 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043d13977322c5b35430e8483d9b0236d806f6b14684889623c14ef32a2e4787`  
		Last Modified: Sat, 12 Nov 2022 06:38:29 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; arm variant v6

```console
$ docker pull notary@sha256:1f82c0dbbc82bd59fbf93f527d7f2ffbd8fc1ed12a8da4c60532973cff5a05c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7135948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64884ecdc094e3a451c4a0d38a31f16f339236b9b4b7d44939b82dfd361ebb0`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:53:33 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 04:53:47 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 12 Nov 2022 04:53:47 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 12 Nov 2022 04:53:47 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 04:53:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 04:53:47 GMT
WORKDIR /notary/signer
# Sat, 12 Nov 2022 04:53:47 GMT
COPY /notary-signer ./ # buildkit
# Sat, 12 Nov 2022 04:53:48 GMT
RUN ./notary-signer --version # buildkit
# Sat, 12 Nov 2022 04:53:48 GMT
COPY ./signer-config.json . # buildkit
# Sat, 12 Nov 2022 04:53:48 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 04:53:48 GMT
USER notary
# Sat, 12 Nov 2022 04:53:48 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 04:53:48 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962f84bc6be5fe2d32e4441665bf4590588a5e805f0f4dc59ca7f20062278a1a`  
		Last Modified: Sat, 12 Nov 2022 04:54:08 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125649f53222ca94f2e22db8ba79ba38d7d33fee96be71c6f2a0e58b1045ac49`  
		Last Modified: Sat, 12 Nov 2022 04:54:19 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b067c75c34c77df098051215649c6c0a8e91da9b069631185bc4f43552cdb008`  
		Last Modified: Sat, 12 Nov 2022 04:54:20 GMT  
		Size: 4.5 MB (4518718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887da1571ffb753050d4233e6ca65667b414bdab8e6b7c5fdada89eb4adf9329`  
		Last Modified: Sat, 12 Nov 2022 04:54:19 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76426b68b449dcb14bbd68fab31fa2f8ec7e1fe8a4967cf9da1d82fa1556c9e`  
		Last Modified: Sat, 12 Nov 2022 04:54:19 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045d2087036baa7a9e416eb846827639481ab99ffe9dfd8adf8bab3523c8f717`  
		Last Modified: Sat, 12 Nov 2022 04:54:19 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:6f5f4e8131ea03706d970d0246a927c3d53f435f32245a886e376564d6de3985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7093202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06f0148bae40fc4e6af75c833b0c136f7907e50fc7b73e0bbb40cc8bae0a63d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:36:49 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 04:36:54 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 12 Nov 2022 04:36:54 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 12 Nov 2022 04:36:54 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 04:36:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 04:36:54 GMT
WORKDIR /notary/signer
# Sat, 12 Nov 2022 04:36:54 GMT
COPY /notary-signer ./ # buildkit
# Sat, 12 Nov 2022 04:36:55 GMT
RUN ./notary-signer --version # buildkit
# Sat, 12 Nov 2022 04:36:55 GMT
COPY ./signer-config.json . # buildkit
# Sat, 12 Nov 2022 04:36:55 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 04:36:55 GMT
USER notary
# Sat, 12 Nov 2022 04:36:55 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 04:36:55 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d302558fe89c8fe780469f0b8d23bc5062a020060a765fb3f2fbf0d7504a640`  
		Last Modified: Sat, 12 Nov 2022 04:37:07 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92adb73f02c38f4aa06f3e987ca18858a12b469b490a35a7fb86b341f2b68fb4`  
		Last Modified: Sat, 12 Nov 2022 04:37:16 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f4534f74420a6707e247e56d44fb30f5fcfeb1bac1e96b70672bb13b362ace`  
		Last Modified: Sat, 12 Nov 2022 04:37:16 GMT  
		Size: 4.4 MB (4383290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6241ea4149079f8c74be251b95022fd118ff1b81741e8f5d599d09b5c1b26f80`  
		Last Modified: Sat, 12 Nov 2022 04:37:16 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d438ce847e1fb4cb73e893a3250887497305e431729d185fd704a98faa25265`  
		Last Modified: Sat, 12 Nov 2022 04:37:16 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bdfeb8c515422b448dcee3e98dc11b02fd15d284c31646030292525bfc85d27`  
		Last Modified: Sat, 12 Nov 2022 04:37:16 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; 386

```console
$ docker pull notary@sha256:ccf760baa69a000366616a0a8483227fe958d9552e0bb5c5350ac67a3349ad03
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a228cadcdf89fde34544574caec4c7aeb4900c9e0c01720d621efb48b877ea70`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:57:54 GMT
RUN adduser -D -H -g "" notary
# Sat, 12 Nov 2022 04:58:12 GMT
EXPOSE 4444
# Sat, 12 Nov 2022 04:58:12 GMT
EXPOSE 7899
# Sat, 12 Nov 2022 04:58:13 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 04:58:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 04:58:15 GMT
WORKDIR /notary/signer
# Tue, 15 Nov 2022 23:10:52 GMT
COPY file:d49fc68cb688349d610a34c45e5f8d83635a2ab9f146d30a02c47f2ad7de33e7 in ./ 
# Tue, 15 Nov 2022 23:10:52 GMT
RUN ./notary-signer --version
# Tue, 15 Nov 2022 23:10:54 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Tue, 15 Nov 2022 23:10:55 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Tue, 15 Nov 2022 23:10:55 GMT
USER notary
# Tue, 15 Nov 2022 23:10:56 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 15 Nov 2022 23:10:57 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e2a37344f15c9c47f28fb76d0bbfae6f9adb65b4d686216a9a5881505ed0ec`  
		Last Modified: Sat, 12 Nov 2022 04:58:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26472dc994c1e659b114a40b8becb18e4595de57079b3495843fe3ee077329d`  
		Last Modified: Sat, 12 Nov 2022 04:58:51 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a2bb9648ddeb3650f07f31e19b9daeb68811be30890823779495e2c038e986`  
		Last Modified: Tue, 15 Nov 2022 23:11:24 GMT  
		Size: 4.6 MB (4571171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5e15d8c601f2d09cffc7529e883783c963a83f02c0f139f4a61d59f84f8a76`  
		Last Modified: Tue, 15 Nov 2022 23:11:23 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7787936793e92bc034fc5c066e78b9ed0040e1d158264e8d4c67ca9420ff8451`  
		Last Modified: Tue, 15 Nov 2022 23:11:23 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; ppc64le

```console
$ docker pull notary@sha256:34b0527222f98b31d9033e7dc0cb2d6454c02c250ce650208ef60fb6710fee9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7096099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdcf81ce9650d09e0485d8213b46bef66e4a95370a0466a131b849c2cbff44d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:12:27 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 07:12:40 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 12 Nov 2022 07:12:40 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 12 Nov 2022 07:12:40 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 07:12:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 07:12:40 GMT
WORKDIR /notary/signer
# Sat, 12 Nov 2022 07:12:41 GMT
COPY /notary-signer ./ # buildkit
# Sat, 12 Nov 2022 07:12:41 GMT
RUN ./notary-signer --version # buildkit
# Sat, 12 Nov 2022 07:12:42 GMT
COPY ./signer-config.json . # buildkit
# Sat, 12 Nov 2022 07:12:42 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 07:12:42 GMT
USER notary
# Sat, 12 Nov 2022 07:12:42 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 07:12:42 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15023fe5082ace3d77a3ca4c98a9b31b5bef60a4835bddce618606ee9f17cf6`  
		Last Modified: Sat, 12 Nov 2022 07:13:02 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca3c7abc8ed18b90618dae3d8ed39fa05a0357ae27fab896191fb471938ae78`  
		Last Modified: Sat, 12 Nov 2022 07:13:14 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860b7bc0efea8be44f360d4e3f045eb869438e6042e750a55da16f987d4055e1`  
		Last Modified: Sat, 12 Nov 2022 07:13:15 GMT  
		Size: 4.3 MB (4292387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e649fba644b3b98a8479f45235bdac31945daf113e21b3fdc5fde0f7e9b68003`  
		Last Modified: Sat, 12 Nov 2022 07:13:13 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222eadf708b86c23df927652dd87eca37256074513de732b94684f62f822d32a`  
		Last Modified: Sat, 12 Nov 2022 07:13:13 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198d4db70d96183d1112cfb2a62b8088e375108784b3e70f2e10b1209c7afd2b`  
		Last Modified: Sat, 12 Nov 2022 07:13:14 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; s390x

```console
$ docker pull notary@sha256:d5d6b8e5f4c93c3063aadc7ebfc46e8802f2931a88c60b0d31b323f4e4bc7f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b4ae846424627d1bc27fd82d9c4b174269d2c260a6820d6e331055beaa2cd1`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:42:05 GMT
ADD file:b78ae95cbacd853e398f187adaf3be51d9e301a66de8f7a4b6c60a9733075cb5 in / 
# Sat, 12 Nov 2022 03:42:06 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:29:11 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 05:29:25 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 12 Nov 2022 05:29:25 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 12 Nov 2022 05:29:25 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 05:29:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 05:29:25 GMT
WORKDIR /notary/signer
# Sat, 12 Nov 2022 05:29:26 GMT
COPY /notary-signer ./ # buildkit
# Sat, 12 Nov 2022 05:29:27 GMT
RUN ./notary-signer --version # buildkit
# Sat, 12 Nov 2022 05:29:27 GMT
COPY ./signer-config.json . # buildkit
# Sat, 12 Nov 2022 05:29:27 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 05:29:27 GMT
USER notary
# Sat, 12 Nov 2022 05:29:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 05:29:27 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:cff16a5ffe2df97bc1d10b021c5ceb98bdb36a18a1d70395590444ac204a9b2b`  
		Last Modified: Sat, 12 Nov 2022 03:43:06 GMT  
		Size: 2.6 MB (2591126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4ef31691b8350e3f169efda08440ffc8f858999b921631575acdfd35d88225`  
		Last Modified: Sat, 12 Nov 2022 05:29:49 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab5959c551fe4b84515f58281a78c8105c856e6509e5d6d5f6140438605e776`  
		Last Modified: Sat, 12 Nov 2022 05:29:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4082365898c22a5e5e3d1dee40f02a634992078f8ac4d9d5b8ee9fb99ac62fe`  
		Last Modified: Sat, 12 Nov 2022 05:29:57 GMT  
		Size: 4.6 MB (4601212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476a971d17cb5d00bbe9b2644e4a92fcd83fb9bfe7028a5f262a5416598d0903`  
		Last Modified: Sat, 12 Nov 2022 05:30:06 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e42c0b96010dbeeb8e7d26d4661e7b16b82d218bdc64b291629c46a3a4572c1`  
		Last Modified: Sat, 12 Nov 2022 05:29:57 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81642580798949db05806bb1ee469fe6f8d454aa5fba863d6a9d00cc586c572`  
		Last Modified: Sat, 12 Nov 2022 05:29:56 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:signer-0.7.0`

```console
$ docker pull notary@sha256:bb75b00e2ad22777b0073e0e29ae8a21d45e0ce4fbe535b4d95313a6280b4267
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
$ docker pull notary@sha256:55cade7712a7a99cd80e60f3cacc1a51ed29da4d6597d66c08313a70dbb9c8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7565226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0c93846d65121b8323f16ef2806bbecec97aabef96a991262f99a0b1be473a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:38:02 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 06:38:08 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 12 Nov 2022 06:38:08 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 12 Nov 2022 06:38:08 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 06:38:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 06:38:08 GMT
WORKDIR /notary/signer
# Sat, 12 Nov 2022 06:38:08 GMT
COPY /notary-signer ./ # buildkit
# Sat, 12 Nov 2022 06:38:08 GMT
RUN ./notary-signer --version # buildkit
# Sat, 12 Nov 2022 06:38:08 GMT
COPY ./signer-config.json . # buildkit
# Sat, 12 Nov 2022 06:38:08 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 06:38:08 GMT
USER notary
# Sat, 12 Nov 2022 06:38:08 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 06:38:08 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab556644ad7457163fa974396862be0db6a3e9b2a288041b04e6009ae65f4ed`  
		Last Modified: Sat, 12 Nov 2022 06:38:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da59cda2c120691b5be31fdc1571f10856ae5c4527c577ae2f76cd70fcd4a05`  
		Last Modified: Sat, 12 Nov 2022 06:38:29 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c81e7e77b856a4b227f55f4c046dd4a3552e7f3e26f324115728eedf3fddd4`  
		Last Modified: Sat, 12 Nov 2022 06:38:30 GMT  
		Size: 4.8 MB (4756800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cc590c46cc2073e2d2ad5b086f723684d1fec0b2a793fda8366aa6af523b16`  
		Last Modified: Sat, 12 Nov 2022 06:38:29 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c48c354c6b48571de1465f8c01053e9a2eb9a38d245a863094ad3cdd6bd141`  
		Last Modified: Sat, 12 Nov 2022 06:38:29 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043d13977322c5b35430e8483d9b0236d806f6b14684889623c14ef32a2e4787`  
		Last Modified: Sat, 12 Nov 2022 06:38:29 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:1f82c0dbbc82bd59fbf93f527d7f2ffbd8fc1ed12a8da4c60532973cff5a05c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7135948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64884ecdc094e3a451c4a0d38a31f16f339236b9b4b7d44939b82dfd361ebb0`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:53:33 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 04:53:47 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 12 Nov 2022 04:53:47 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 12 Nov 2022 04:53:47 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 04:53:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 04:53:47 GMT
WORKDIR /notary/signer
# Sat, 12 Nov 2022 04:53:47 GMT
COPY /notary-signer ./ # buildkit
# Sat, 12 Nov 2022 04:53:48 GMT
RUN ./notary-signer --version # buildkit
# Sat, 12 Nov 2022 04:53:48 GMT
COPY ./signer-config.json . # buildkit
# Sat, 12 Nov 2022 04:53:48 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 04:53:48 GMT
USER notary
# Sat, 12 Nov 2022 04:53:48 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 04:53:48 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962f84bc6be5fe2d32e4441665bf4590588a5e805f0f4dc59ca7f20062278a1a`  
		Last Modified: Sat, 12 Nov 2022 04:54:08 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125649f53222ca94f2e22db8ba79ba38d7d33fee96be71c6f2a0e58b1045ac49`  
		Last Modified: Sat, 12 Nov 2022 04:54:19 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b067c75c34c77df098051215649c6c0a8e91da9b069631185bc4f43552cdb008`  
		Last Modified: Sat, 12 Nov 2022 04:54:20 GMT  
		Size: 4.5 MB (4518718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887da1571ffb753050d4233e6ca65667b414bdab8e6b7c5fdada89eb4adf9329`  
		Last Modified: Sat, 12 Nov 2022 04:54:19 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76426b68b449dcb14bbd68fab31fa2f8ec7e1fe8a4967cf9da1d82fa1556c9e`  
		Last Modified: Sat, 12 Nov 2022 04:54:19 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045d2087036baa7a9e416eb846827639481ab99ffe9dfd8adf8bab3523c8f717`  
		Last Modified: Sat, 12 Nov 2022 04:54:19 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:6f5f4e8131ea03706d970d0246a927c3d53f435f32245a886e376564d6de3985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7093202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06f0148bae40fc4e6af75c833b0c136f7907e50fc7b73e0bbb40cc8bae0a63d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:36:49 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 04:36:54 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 12 Nov 2022 04:36:54 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 12 Nov 2022 04:36:54 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 04:36:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 04:36:54 GMT
WORKDIR /notary/signer
# Sat, 12 Nov 2022 04:36:54 GMT
COPY /notary-signer ./ # buildkit
# Sat, 12 Nov 2022 04:36:55 GMT
RUN ./notary-signer --version # buildkit
# Sat, 12 Nov 2022 04:36:55 GMT
COPY ./signer-config.json . # buildkit
# Sat, 12 Nov 2022 04:36:55 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 04:36:55 GMT
USER notary
# Sat, 12 Nov 2022 04:36:55 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 04:36:55 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d302558fe89c8fe780469f0b8d23bc5062a020060a765fb3f2fbf0d7504a640`  
		Last Modified: Sat, 12 Nov 2022 04:37:07 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92adb73f02c38f4aa06f3e987ca18858a12b469b490a35a7fb86b341f2b68fb4`  
		Last Modified: Sat, 12 Nov 2022 04:37:16 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f4534f74420a6707e247e56d44fb30f5fcfeb1bac1e96b70672bb13b362ace`  
		Last Modified: Sat, 12 Nov 2022 04:37:16 GMT  
		Size: 4.4 MB (4383290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6241ea4149079f8c74be251b95022fd118ff1b81741e8f5d599d09b5c1b26f80`  
		Last Modified: Sat, 12 Nov 2022 04:37:16 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d438ce847e1fb4cb73e893a3250887497305e431729d185fd704a98faa25265`  
		Last Modified: Sat, 12 Nov 2022 04:37:16 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bdfeb8c515422b448dcee3e98dc11b02fd15d284c31646030292525bfc85d27`  
		Last Modified: Sat, 12 Nov 2022 04:37:16 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:ccf760baa69a000366616a0a8483227fe958d9552e0bb5c5350ac67a3349ad03
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a228cadcdf89fde34544574caec4c7aeb4900c9e0c01720d621efb48b877ea70`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:57:54 GMT
RUN adduser -D -H -g "" notary
# Sat, 12 Nov 2022 04:58:12 GMT
EXPOSE 4444
# Sat, 12 Nov 2022 04:58:12 GMT
EXPOSE 7899
# Sat, 12 Nov 2022 04:58:13 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 04:58:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 04:58:15 GMT
WORKDIR /notary/signer
# Tue, 15 Nov 2022 23:10:52 GMT
COPY file:d49fc68cb688349d610a34c45e5f8d83635a2ab9f146d30a02c47f2ad7de33e7 in ./ 
# Tue, 15 Nov 2022 23:10:52 GMT
RUN ./notary-signer --version
# Tue, 15 Nov 2022 23:10:54 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Tue, 15 Nov 2022 23:10:55 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Tue, 15 Nov 2022 23:10:55 GMT
USER notary
# Tue, 15 Nov 2022 23:10:56 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 15 Nov 2022 23:10:57 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e2a37344f15c9c47f28fb76d0bbfae6f9adb65b4d686216a9a5881505ed0ec`  
		Last Modified: Sat, 12 Nov 2022 04:58:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26472dc994c1e659b114a40b8becb18e4595de57079b3495843fe3ee077329d`  
		Last Modified: Sat, 12 Nov 2022 04:58:51 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a2bb9648ddeb3650f07f31e19b9daeb68811be30890823779495e2c038e986`  
		Last Modified: Tue, 15 Nov 2022 23:11:24 GMT  
		Size: 4.6 MB (4571171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5e15d8c601f2d09cffc7529e883783c963a83f02c0f139f4a61d59f84f8a76`  
		Last Modified: Tue, 15 Nov 2022 23:11:23 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7787936793e92bc034fc5c066e78b9ed0040e1d158264e8d4c67ca9420ff8451`  
		Last Modified: Tue, 15 Nov 2022 23:11:23 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:34b0527222f98b31d9033e7dc0cb2d6454c02c250ce650208ef60fb6710fee9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7096099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdcf81ce9650d09e0485d8213b46bef66e4a95370a0466a131b849c2cbff44d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:12:27 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 07:12:40 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 12 Nov 2022 07:12:40 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 12 Nov 2022 07:12:40 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 07:12:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 07:12:40 GMT
WORKDIR /notary/signer
# Sat, 12 Nov 2022 07:12:41 GMT
COPY /notary-signer ./ # buildkit
# Sat, 12 Nov 2022 07:12:41 GMT
RUN ./notary-signer --version # buildkit
# Sat, 12 Nov 2022 07:12:42 GMT
COPY ./signer-config.json . # buildkit
# Sat, 12 Nov 2022 07:12:42 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 07:12:42 GMT
USER notary
# Sat, 12 Nov 2022 07:12:42 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 07:12:42 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15023fe5082ace3d77a3ca4c98a9b31b5bef60a4835bddce618606ee9f17cf6`  
		Last Modified: Sat, 12 Nov 2022 07:13:02 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca3c7abc8ed18b90618dae3d8ed39fa05a0357ae27fab896191fb471938ae78`  
		Last Modified: Sat, 12 Nov 2022 07:13:14 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860b7bc0efea8be44f360d4e3f045eb869438e6042e750a55da16f987d4055e1`  
		Last Modified: Sat, 12 Nov 2022 07:13:15 GMT  
		Size: 4.3 MB (4292387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e649fba644b3b98a8479f45235bdac31945daf113e21b3fdc5fde0f7e9b68003`  
		Last Modified: Sat, 12 Nov 2022 07:13:13 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222eadf708b86c23df927652dd87eca37256074513de732b94684f62f822d32a`  
		Last Modified: Sat, 12 Nov 2022 07:13:13 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198d4db70d96183d1112cfb2a62b8088e375108784b3e70f2e10b1209c7afd2b`  
		Last Modified: Sat, 12 Nov 2022 07:13:14 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:d5d6b8e5f4c93c3063aadc7ebfc46e8802f2931a88c60b0d31b323f4e4bc7f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b4ae846424627d1bc27fd82d9c4b174269d2c260a6820d6e331055beaa2cd1`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:42:05 GMT
ADD file:b78ae95cbacd853e398f187adaf3be51d9e301a66de8f7a4b6c60a9733075cb5 in / 
# Sat, 12 Nov 2022 03:42:06 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:29:11 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 05:29:25 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 12 Nov 2022 05:29:25 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 12 Nov 2022 05:29:25 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 05:29:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 05:29:25 GMT
WORKDIR /notary/signer
# Sat, 12 Nov 2022 05:29:26 GMT
COPY /notary-signer ./ # buildkit
# Sat, 12 Nov 2022 05:29:27 GMT
RUN ./notary-signer --version # buildkit
# Sat, 12 Nov 2022 05:29:27 GMT
COPY ./signer-config.json . # buildkit
# Sat, 12 Nov 2022 05:29:27 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 12 Nov 2022 05:29:27 GMT
USER notary
# Sat, 12 Nov 2022 05:29:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 12 Nov 2022 05:29:27 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:cff16a5ffe2df97bc1d10b021c5ceb98bdb36a18a1d70395590444ac204a9b2b`  
		Last Modified: Sat, 12 Nov 2022 03:43:06 GMT  
		Size: 2.6 MB (2591126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4ef31691b8350e3f169efda08440ffc8f858999b921631575acdfd35d88225`  
		Last Modified: Sat, 12 Nov 2022 05:29:49 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab5959c551fe4b84515f58281a78c8105c856e6509e5d6d5f6140438605e776`  
		Last Modified: Sat, 12 Nov 2022 05:29:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4082365898c22a5e5e3d1dee40f02a634992078f8ac4d9d5b8ee9fb99ac62fe`  
		Last Modified: Sat, 12 Nov 2022 05:29:57 GMT  
		Size: 4.6 MB (4601212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476a971d17cb5d00bbe9b2644e4a92fcd83fb9bfe7028a5f262a5416598d0903`  
		Last Modified: Sat, 12 Nov 2022 05:30:06 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e42c0b96010dbeeb8e7d26d4661e7b16b82d218bdc64b291629c46a3a4572c1`  
		Last Modified: Sat, 12 Nov 2022 05:29:57 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81642580798949db05806bb1ee469fe6f8d454aa5fba863d6a9d00cc586c572`  
		Last Modified: Sat, 12 Nov 2022 05:29:56 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
