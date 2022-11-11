<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `notary`

-	[`notary:server`](#notaryserver)
-	[`notary:server-0.7.0`](#notaryserver-070)
-	[`notary:signer`](#notarysigner)
-	[`notary:signer-0.7.0`](#notarysigner-070)

## `notary:server`

```console
$ docker pull notary@sha256:0af9388e5680b41804802a8c24a4b80d9fec8c528021ffacb5f47c56e204e639
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
$ docker pull notary@sha256:725646c4d072977023698a3c1b25fc68862ed1646e26b7f8ae60ad7c2549a59e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9925dcb4c27e30de0f81ce854368e4f7c8246d84b40e220ca2aa581b356543`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 01:52:21 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 01:52:21 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 25 Oct 2022 01:52:21 GMT
ENV INSTALLDIR=/notary/server
# Tue, 25 Oct 2022 01:52:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 25 Oct 2022 01:52:21 GMT
WORKDIR /notary/server
# Tue, 01 Nov 2022 19:49:00 GMT
COPY /notary-server ./ # buildkit
# Tue, 01 Nov 2022 19:49:00 GMT
RUN ./notary-server --version # buildkit
# Tue, 01 Nov 2022 19:49:00 GMT
COPY ./server-config.json . # buildkit
# Tue, 01 Nov 2022 19:49:00 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 01 Nov 2022 19:49:00 GMT
USER notary
# Tue, 01 Nov 2022 19:49:00 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:49:00 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ae0db85ee62912972b015b43b47b5849f5b66900a08ad146a42f7c16d02def`  
		Last Modified: Tue, 25 Oct 2022 01:53:00 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae714b9c46c68b869025bf262b5afec2bb7f99f3739cdae14e11604248f87fd`  
		Last Modified: Tue, 25 Oct 2022 01:52:58 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288b5f0093c5cb556b6e816cc8c65e59ea4a3be57cd8c9cfbab00dbe5bcdb49c`  
		Last Modified: Tue, 01 Nov 2022 19:49:21 GMT  
		Size: 5.1 MB (5143673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca8a52dd6617ccfc327338630a16dcd2ef53f59ec3014397fd87e6ace50c555`  
		Last Modified: Tue, 01 Nov 2022 19:49:20 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5a71241ee3d85608914a3d2c7779ce29252304f4225ad71dcfe3c1b046f3a2`  
		Last Modified: Tue, 01 Nov 2022 19:49:20 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c863d998853c7cbc0e52dbf21a83074cbc3f2acc5cec1f9cb7992d95cffe7e`  
		Last Modified: Tue, 01 Nov 2022 19:49:20 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm variant v6

```console
$ docker pull notary@sha256:0ca279421c9b89277046af0d03ffa5e634035874ed7546ab02ec0b9a08f9adb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40338717be867b42b831b4184924a76cfe5412b004a276b053d1cf4270d6db6`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 05:30:38 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 05:30:38 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 25 Oct 2022 05:30:38 GMT
ENV INSTALLDIR=/notary/server
# Tue, 25 Oct 2022 05:30:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 25 Oct 2022 05:30:38 GMT
WORKDIR /notary/server
# Tue, 01 Nov 2022 19:20:13 GMT
COPY /notary-server ./ # buildkit
# Tue, 01 Nov 2022 19:20:13 GMT
RUN ./notary-server --version # buildkit
# Tue, 01 Nov 2022 19:20:13 GMT
COPY ./server-config.json . # buildkit
# Tue, 01 Nov 2022 19:20:13 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 01 Nov 2022 19:20:13 GMT
USER notary
# Tue, 01 Nov 2022 19:20:13 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:20:13 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719245ee64918db6e14bc8a74787353276669a8486a5743651ec04a1872a4357`  
		Last Modified: Tue, 25 Oct 2022 05:31:43 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507f3b2412355e8361b78d3945186fcdf4be76d2e96b01137a4c3e9ee7a93ce0`  
		Last Modified: Tue, 25 Oct 2022 05:31:41 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218f43ba2723b67fb886756e06cec7a11656934d9547bf1d9086215bcd9a2a48`  
		Last Modified: Tue, 01 Nov 2022 19:20:47 GMT  
		Size: 4.9 MB (4888306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e9be78df3a3476eda8fe203e6a17d409a906e42d517a0bf3a49c09a95b2684`  
		Last Modified: Tue, 01 Nov 2022 19:20:46 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb29581966cd0c497c545394b742d5ab93ec3a373fe174fd47d8de83196487`  
		Last Modified: Tue, 01 Nov 2022 19:20:46 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74ba7c6f9b6e9c0b92cccd991a419aa00759ea44493c09c68241c53a6efb309`  
		Last Modified: Tue, 01 Nov 2022 19:20:46 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:d6951d769b06537a098bb49129fc25f4579270719ea1819890fb247520ad9ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e565deff06d0ab3274f69512f6c80183104474faa451986d483b06afe691707`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Thu, 10 Nov 2022 20:39:41 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 05:54:03 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 05:54:03 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 25 Oct 2022 05:54:03 GMT
ENV INSTALLDIR=/notary/server
# Tue, 25 Oct 2022 05:54:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 25 Oct 2022 05:54:03 GMT
WORKDIR /notary/server
# Thu, 10 Nov 2022 23:37:49 GMT
COPY /notary-server ./ # buildkit
# Thu, 10 Nov 2022 23:37:49 GMT
RUN ./notary-server --version # buildkit
# Thu, 10 Nov 2022 23:37:49 GMT
COPY ./server-config.json . # buildkit
# Thu, 10 Nov 2022 23:37:49 GMT
COPY ./entrypoint.sh . # buildkit
# Thu, 10 Nov 2022 23:37:49 GMT
USER notary
# Thu, 10 Nov 2022 23:37:49 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 10 Nov 2022 23:37:49 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19c11ef8813c7c7e52078792213cc1951b797dfeda0933eb53237672542be0d`  
		Last Modified: Tue, 25 Oct 2022 05:54:34 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19eb1e9176b5da3983b2cb1e27af9a2fa727b656a122553479f995fbf2b46e1b`  
		Last Modified: Tue, 25 Oct 2022 05:54:31 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ea168370e76af6d291297e73e4f23e1893896e9af9685f80713192a94d5f91`  
		Last Modified: Thu, 10 Nov 2022 23:38:08 GMT  
		Size: 4.7 MB (4731490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4507a254e830b65e442c31b62ab1b203dbb73f3d7ed0bd2544ebc0c38f0d562e`  
		Last Modified: Thu, 10 Nov 2022 23:38:07 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46631128d534c955012e6545662f6ce3727970edc3fd92995e67f0b98b717a5`  
		Last Modified: Thu, 10 Nov 2022 23:38:07 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36385a6b8d65e2d4ae7d454a58c0883ae01a3236e4f3081b11ee378833f1010f`  
		Last Modified: Thu, 10 Nov 2022 23:38:07 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; 386

```console
$ docker pull notary@sha256:56985e83fdafdbcfa5ccf1997cc2e91ec65b3e0ef09c6083a1c3f98d36600ab0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7753716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2eda2b920344af93839f627b00c8ad8377a76ede8c15b537d94edd82ddc7963`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 02:33:41 GMT
RUN adduser -D -H -g "" notary
# Tue, 25 Oct 2022 02:33:42 GMT
EXPOSE 4443
# Tue, 25 Oct 2022 02:33:43 GMT
ENV INSTALLDIR=/notary/server
# Tue, 25 Oct 2022 02:33:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 25 Oct 2022 02:33:45 GMT
WORKDIR /notary/server
# Tue, 01 Nov 2022 19:09:52 GMT
COPY file:0a1052f2e85f22b78af7f4b75052a7720366ea3e414c533f54520e6b3a594392 in ./ 
# Tue, 01 Nov 2022 19:09:52 GMT
RUN ./notary-server --version
# Tue, 01 Nov 2022 19:09:54 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Tue, 01 Nov 2022 19:09:55 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Tue, 01 Nov 2022 19:09:55 GMT
USER notary
# Tue, 01 Nov 2022 19:09:56 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:09:57 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c692a1d61ff49f4083804ea05880254cdbf59904eff09aa2c9284e77eed914b`  
		Last Modified: Tue, 25 Oct 2022 02:34:26 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3d42d44a8b5ecb98b422ef1b15781ffa3f5b72a6f1f05f7de4c10f738d4e12`  
		Last Modified: Tue, 25 Oct 2022 02:34:26 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79893d0157be3c219706bec77f9f7a01e497add3eaefb7a17913ec798b1e08ad`  
		Last Modified: Tue, 01 Nov 2022 19:10:27 GMT  
		Size: 4.9 MB (4944483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e4fb9707ded5f0d42b069b2e17a52379fc239e44e012f15db2fa09e7b3b100`  
		Last Modified: Tue, 01 Nov 2022 19:10:27 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f3b6eaf9eaad5dc428d585608f9c48885621699eb177eeba557a789af0da33`  
		Last Modified: Tue, 01 Nov 2022 19:10:27 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; ppc64le

```console
$ docker pull notary@sha256:4ca31bfcdb4a6d89b58aa9f067d597229713d7d5275543c8dc6b8931eed2b558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7438784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaffe1ddf7527db170da86817e9d28b6ba910c80c1cb1af2ce64ba007b379ff6`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 03:23:54 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 03:23:54 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 25 Oct 2022 03:23:54 GMT
ENV INSTALLDIR=/notary/server
# Tue, 25 Oct 2022 03:23:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 25 Oct 2022 03:23:54 GMT
WORKDIR /notary/server
# Tue, 01 Nov 2022 19:52:44 GMT
COPY /notary-server ./ # buildkit
# Tue, 01 Nov 2022 19:52:45 GMT
RUN ./notary-server --version # buildkit
# Tue, 01 Nov 2022 19:52:45 GMT
COPY ./server-config.json . # buildkit
# Tue, 01 Nov 2022 19:52:46 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 01 Nov 2022 19:52:46 GMT
USER notary
# Tue, 01 Nov 2022 19:52:46 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:52:46 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28847305e982967909062e053ecacc81ae6035a3f7b3587b0e54677ab21f709c`  
		Last Modified: Tue, 25 Oct 2022 03:25:00 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7d5711e3906a11f7dc77d3091b7991f23e497d88cd28b0d987afae0a8d597f`  
		Last Modified: Tue, 25 Oct 2022 03:24:57 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15db5598874eb3b3ecd9bb5c44cb36d683a05e4313c56aaf88b63babed2b8182`  
		Last Modified: Tue, 01 Nov 2022 19:53:19 GMT  
		Size: 4.6 MB (4633225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe346e270ce2d6d41eeb31a763b028ebe66b6aefe9aae57784708949e29f1da`  
		Last Modified: Tue, 01 Nov 2022 19:53:17 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3267ca5eea7a1a7caad2876f477ab40b3c51b3f0eea788f81aa387097710b81`  
		Last Modified: Tue, 01 Nov 2022 19:53:17 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a44ccd55cd93121224074cecdb36f928912b551da93ffb74da116d8abc17dac`  
		Last Modified: Tue, 01 Nov 2022 19:53:18 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; s390x

```console
$ docker pull notary@sha256:e0bf9c880e5857c4043e9a6fec00f472a2f19af198192a5189c36afc6c1155c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7561572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f6b49a52a7439412f8c0d05706851e5e327b29cf9bd71177f3924a1489347c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 01:21:39 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 01:21:39 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 25 Oct 2022 01:21:39 GMT
ENV INSTALLDIR=/notary/server
# Tue, 25 Oct 2022 01:21:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 25 Oct 2022 01:21:39 GMT
WORKDIR /notary/server
# Tue, 01 Nov 2022 19:22:59 GMT
COPY /notary-server ./ # buildkit
# Tue, 01 Nov 2022 19:22:59 GMT
RUN ./notary-server --version # buildkit
# Tue, 01 Nov 2022 19:23:00 GMT
COPY ./server-config.json . # buildkit
# Tue, 01 Nov 2022 19:23:00 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 01 Nov 2022 19:23:00 GMT
USER notary
# Tue, 01 Nov 2022 19:23:00 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:23:00 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e57b7c2a2dbd108e38c96fd7b110170d3b57a921f34c3b015736a93b17e5ad`  
		Last Modified: Tue, 25 Oct 2022 01:22:34 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb73212e82f7d46920138e024d3233301bdffa778ba147338014ae69d65ba43c`  
		Last Modified: Tue, 25 Oct 2022 01:22:33 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0b0f1ca5387a892ad627d97e99e96b30cad174a591dbe1375adac0a87db741`  
		Last Modified: Tue, 01 Nov 2022 19:23:39 GMT  
		Size: 5.0 MB (4968737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203dfc74ac5ba65a949de65aec38016eacb8fe750fe2e5357924559bbd6e5afe`  
		Last Modified: Tue, 01 Nov 2022 19:23:39 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362dedb8e4f58a86a6e7e5965a12eb241b599dc6949f68b22217026f2f3857e5`  
		Last Modified: Tue, 01 Nov 2022 19:23:38 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce527d322ebdd7c3f241053ee30c18e1fa62d83d7449a6c2237a4e32af7c7fea`  
		Last Modified: Tue, 01 Nov 2022 19:23:38 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:server-0.7.0`

```console
$ docker pull notary@sha256:0af9388e5680b41804802a8c24a4b80d9fec8c528021ffacb5f47c56e204e639
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
$ docker pull notary@sha256:725646c4d072977023698a3c1b25fc68862ed1646e26b7f8ae60ad7c2549a59e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9925dcb4c27e30de0f81ce854368e4f7c8246d84b40e220ca2aa581b356543`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 01:52:21 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 01:52:21 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 25 Oct 2022 01:52:21 GMT
ENV INSTALLDIR=/notary/server
# Tue, 25 Oct 2022 01:52:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 25 Oct 2022 01:52:21 GMT
WORKDIR /notary/server
# Tue, 01 Nov 2022 19:49:00 GMT
COPY /notary-server ./ # buildkit
# Tue, 01 Nov 2022 19:49:00 GMT
RUN ./notary-server --version # buildkit
# Tue, 01 Nov 2022 19:49:00 GMT
COPY ./server-config.json . # buildkit
# Tue, 01 Nov 2022 19:49:00 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 01 Nov 2022 19:49:00 GMT
USER notary
# Tue, 01 Nov 2022 19:49:00 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:49:00 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ae0db85ee62912972b015b43b47b5849f5b66900a08ad146a42f7c16d02def`  
		Last Modified: Tue, 25 Oct 2022 01:53:00 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae714b9c46c68b869025bf262b5afec2bb7f99f3739cdae14e11604248f87fd`  
		Last Modified: Tue, 25 Oct 2022 01:52:58 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288b5f0093c5cb556b6e816cc8c65e59ea4a3be57cd8c9cfbab00dbe5bcdb49c`  
		Last Modified: Tue, 01 Nov 2022 19:49:21 GMT  
		Size: 5.1 MB (5143673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca8a52dd6617ccfc327338630a16dcd2ef53f59ec3014397fd87e6ace50c555`  
		Last Modified: Tue, 01 Nov 2022 19:49:20 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5a71241ee3d85608914a3d2c7779ce29252304f4225ad71dcfe3c1b046f3a2`  
		Last Modified: Tue, 01 Nov 2022 19:49:20 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c863d998853c7cbc0e52dbf21a83074cbc3f2acc5cec1f9cb7992d95cffe7e`  
		Last Modified: Tue, 01 Nov 2022 19:49:20 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:0ca279421c9b89277046af0d03ffa5e634035874ed7546ab02ec0b9a08f9adb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40338717be867b42b831b4184924a76cfe5412b004a276b053d1cf4270d6db6`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 05:30:38 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 05:30:38 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 25 Oct 2022 05:30:38 GMT
ENV INSTALLDIR=/notary/server
# Tue, 25 Oct 2022 05:30:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 25 Oct 2022 05:30:38 GMT
WORKDIR /notary/server
# Tue, 01 Nov 2022 19:20:13 GMT
COPY /notary-server ./ # buildkit
# Tue, 01 Nov 2022 19:20:13 GMT
RUN ./notary-server --version # buildkit
# Tue, 01 Nov 2022 19:20:13 GMT
COPY ./server-config.json . # buildkit
# Tue, 01 Nov 2022 19:20:13 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 01 Nov 2022 19:20:13 GMT
USER notary
# Tue, 01 Nov 2022 19:20:13 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:20:13 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719245ee64918db6e14bc8a74787353276669a8486a5743651ec04a1872a4357`  
		Last Modified: Tue, 25 Oct 2022 05:31:43 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507f3b2412355e8361b78d3945186fcdf4be76d2e96b01137a4c3e9ee7a93ce0`  
		Last Modified: Tue, 25 Oct 2022 05:31:41 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218f43ba2723b67fb886756e06cec7a11656934d9547bf1d9086215bcd9a2a48`  
		Last Modified: Tue, 01 Nov 2022 19:20:47 GMT  
		Size: 4.9 MB (4888306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e9be78df3a3476eda8fe203e6a17d409a906e42d517a0bf3a49c09a95b2684`  
		Last Modified: Tue, 01 Nov 2022 19:20:46 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb29581966cd0c497c545394b742d5ab93ec3a373fe174fd47d8de83196487`  
		Last Modified: Tue, 01 Nov 2022 19:20:46 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74ba7c6f9b6e9c0b92cccd991a419aa00759ea44493c09c68241c53a6efb309`  
		Last Modified: Tue, 01 Nov 2022 19:20:46 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:d6951d769b06537a098bb49129fc25f4579270719ea1819890fb247520ad9ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e565deff06d0ab3274f69512f6c80183104474faa451986d483b06afe691707`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Thu, 10 Nov 2022 20:39:41 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 05:54:03 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 05:54:03 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 25 Oct 2022 05:54:03 GMT
ENV INSTALLDIR=/notary/server
# Tue, 25 Oct 2022 05:54:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 25 Oct 2022 05:54:03 GMT
WORKDIR /notary/server
# Thu, 10 Nov 2022 23:37:49 GMT
COPY /notary-server ./ # buildkit
# Thu, 10 Nov 2022 23:37:49 GMT
RUN ./notary-server --version # buildkit
# Thu, 10 Nov 2022 23:37:49 GMT
COPY ./server-config.json . # buildkit
# Thu, 10 Nov 2022 23:37:49 GMT
COPY ./entrypoint.sh . # buildkit
# Thu, 10 Nov 2022 23:37:49 GMT
USER notary
# Thu, 10 Nov 2022 23:37:49 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 10 Nov 2022 23:37:49 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19c11ef8813c7c7e52078792213cc1951b797dfeda0933eb53237672542be0d`  
		Last Modified: Tue, 25 Oct 2022 05:54:34 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19eb1e9176b5da3983b2cb1e27af9a2fa727b656a122553479f995fbf2b46e1b`  
		Last Modified: Tue, 25 Oct 2022 05:54:31 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ea168370e76af6d291297e73e4f23e1893896e9af9685f80713192a94d5f91`  
		Last Modified: Thu, 10 Nov 2022 23:38:08 GMT  
		Size: 4.7 MB (4731490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4507a254e830b65e442c31b62ab1b203dbb73f3d7ed0bd2544ebc0c38f0d562e`  
		Last Modified: Thu, 10 Nov 2022 23:38:07 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46631128d534c955012e6545662f6ce3727970edc3fd92995e67f0b98b717a5`  
		Last Modified: Thu, 10 Nov 2022 23:38:07 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36385a6b8d65e2d4ae7d454a58c0883ae01a3236e4f3081b11ee378833f1010f`  
		Last Modified: Thu, 10 Nov 2022 23:38:07 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:56985e83fdafdbcfa5ccf1997cc2e91ec65b3e0ef09c6083a1c3f98d36600ab0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7753716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2eda2b920344af93839f627b00c8ad8377a76ede8c15b537d94edd82ddc7963`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 02:33:41 GMT
RUN adduser -D -H -g "" notary
# Tue, 25 Oct 2022 02:33:42 GMT
EXPOSE 4443
# Tue, 25 Oct 2022 02:33:43 GMT
ENV INSTALLDIR=/notary/server
# Tue, 25 Oct 2022 02:33:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 25 Oct 2022 02:33:45 GMT
WORKDIR /notary/server
# Tue, 01 Nov 2022 19:09:52 GMT
COPY file:0a1052f2e85f22b78af7f4b75052a7720366ea3e414c533f54520e6b3a594392 in ./ 
# Tue, 01 Nov 2022 19:09:52 GMT
RUN ./notary-server --version
# Tue, 01 Nov 2022 19:09:54 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Tue, 01 Nov 2022 19:09:55 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Tue, 01 Nov 2022 19:09:55 GMT
USER notary
# Tue, 01 Nov 2022 19:09:56 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:09:57 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c692a1d61ff49f4083804ea05880254cdbf59904eff09aa2c9284e77eed914b`  
		Last Modified: Tue, 25 Oct 2022 02:34:26 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3d42d44a8b5ecb98b422ef1b15781ffa3f5b72a6f1f05f7de4c10f738d4e12`  
		Last Modified: Tue, 25 Oct 2022 02:34:26 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79893d0157be3c219706bec77f9f7a01e497add3eaefb7a17913ec798b1e08ad`  
		Last Modified: Tue, 01 Nov 2022 19:10:27 GMT  
		Size: 4.9 MB (4944483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e4fb9707ded5f0d42b069b2e17a52379fc239e44e012f15db2fa09e7b3b100`  
		Last Modified: Tue, 01 Nov 2022 19:10:27 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f3b6eaf9eaad5dc428d585608f9c48885621699eb177eeba557a789af0da33`  
		Last Modified: Tue, 01 Nov 2022 19:10:27 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:4ca31bfcdb4a6d89b58aa9f067d597229713d7d5275543c8dc6b8931eed2b558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7438784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaffe1ddf7527db170da86817e9d28b6ba910c80c1cb1af2ce64ba007b379ff6`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 03:23:54 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 03:23:54 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 25 Oct 2022 03:23:54 GMT
ENV INSTALLDIR=/notary/server
# Tue, 25 Oct 2022 03:23:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 25 Oct 2022 03:23:54 GMT
WORKDIR /notary/server
# Tue, 01 Nov 2022 19:52:44 GMT
COPY /notary-server ./ # buildkit
# Tue, 01 Nov 2022 19:52:45 GMT
RUN ./notary-server --version # buildkit
# Tue, 01 Nov 2022 19:52:45 GMT
COPY ./server-config.json . # buildkit
# Tue, 01 Nov 2022 19:52:46 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 01 Nov 2022 19:52:46 GMT
USER notary
# Tue, 01 Nov 2022 19:52:46 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:52:46 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28847305e982967909062e053ecacc81ae6035a3f7b3587b0e54677ab21f709c`  
		Last Modified: Tue, 25 Oct 2022 03:25:00 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7d5711e3906a11f7dc77d3091b7991f23e497d88cd28b0d987afae0a8d597f`  
		Last Modified: Tue, 25 Oct 2022 03:24:57 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15db5598874eb3b3ecd9bb5c44cb36d683a05e4313c56aaf88b63babed2b8182`  
		Last Modified: Tue, 01 Nov 2022 19:53:19 GMT  
		Size: 4.6 MB (4633225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe346e270ce2d6d41eeb31a763b028ebe66b6aefe9aae57784708949e29f1da`  
		Last Modified: Tue, 01 Nov 2022 19:53:17 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3267ca5eea7a1a7caad2876f477ab40b3c51b3f0eea788f81aa387097710b81`  
		Last Modified: Tue, 01 Nov 2022 19:53:17 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a44ccd55cd93121224074cecdb36f928912b551da93ffb74da116d8abc17dac`  
		Last Modified: Tue, 01 Nov 2022 19:53:18 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:e0bf9c880e5857c4043e9a6fec00f472a2f19af198192a5189c36afc6c1155c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7561572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f6b49a52a7439412f8c0d05706851e5e327b29cf9bd71177f3924a1489347c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 01:21:39 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 01:21:39 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 25 Oct 2022 01:21:39 GMT
ENV INSTALLDIR=/notary/server
# Tue, 25 Oct 2022 01:21:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 25 Oct 2022 01:21:39 GMT
WORKDIR /notary/server
# Tue, 01 Nov 2022 19:22:59 GMT
COPY /notary-server ./ # buildkit
# Tue, 01 Nov 2022 19:22:59 GMT
RUN ./notary-server --version # buildkit
# Tue, 01 Nov 2022 19:23:00 GMT
COPY ./server-config.json . # buildkit
# Tue, 01 Nov 2022 19:23:00 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 01 Nov 2022 19:23:00 GMT
USER notary
# Tue, 01 Nov 2022 19:23:00 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:23:00 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e57b7c2a2dbd108e38c96fd7b110170d3b57a921f34c3b015736a93b17e5ad`  
		Last Modified: Tue, 25 Oct 2022 01:22:34 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb73212e82f7d46920138e024d3233301bdffa778ba147338014ae69d65ba43c`  
		Last Modified: Tue, 25 Oct 2022 01:22:33 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0b0f1ca5387a892ad627d97e99e96b30cad174a591dbe1375adac0a87db741`  
		Last Modified: Tue, 01 Nov 2022 19:23:39 GMT  
		Size: 5.0 MB (4968737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203dfc74ac5ba65a949de65aec38016eacb8fe750fe2e5357924559bbd6e5afe`  
		Last Modified: Tue, 01 Nov 2022 19:23:39 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362dedb8e4f58a86a6e7e5965a12eb241b599dc6949f68b22217026f2f3857e5`  
		Last Modified: Tue, 01 Nov 2022 19:23:38 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce527d322ebdd7c3f241053ee30c18e1fa62d83d7449a6c2237a4e32af7c7fea`  
		Last Modified: Tue, 01 Nov 2022 19:23:38 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:signer`

```console
$ docker pull notary@sha256:1f9e1dae375b5a88b60b6904bd6d95a5147df91e119a849a5152002df047a76b
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
$ docker pull notary@sha256:0a2df6aad290e2b26791851f575d7e51364f1b356895234542e5263114dd0e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7565041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7986ccf50366af23344bbe5e5bea20d70224321eab041ce94bbc227fd28d29`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 01:52:21 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 01:52:46 GMT
EXPOSE map[4444/tcp:{}]
# Tue, 25 Oct 2022 01:52:46 GMT
EXPOSE map[7899/tcp:{}]
# Tue, 25 Oct 2022 01:52:46 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 25 Oct 2022 01:52:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 25 Oct 2022 01:52:46 GMT
WORKDIR /notary/signer
# Tue, 01 Nov 2022 19:49:09 GMT
COPY /notary-signer ./ # buildkit
# Tue, 01 Nov 2022 19:49:10 GMT
RUN ./notary-signer --version # buildkit
# Tue, 01 Nov 2022 19:49:10 GMT
COPY ./signer-config.json . # buildkit
# Tue, 01 Nov 2022 19:49:10 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 01 Nov 2022 19:49:10 GMT
USER notary
# Tue, 01 Nov 2022 19:49:10 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:49:10 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ae0db85ee62912972b015b43b47b5849f5b66900a08ad146a42f7c16d02def`  
		Last Modified: Tue, 25 Oct 2022 01:53:00 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc4162474250e31d2a4a4d6cd0a4f0e9813709d78b77293938ace79068cf662`  
		Last Modified: Tue, 25 Oct 2022 01:53:10 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3192cc45dc578f804bb368238b31cd4f7af695d232971b8cec8a96473f753d4`  
		Last Modified: Tue, 01 Nov 2022 19:49:31 GMT  
		Size: 4.8 MB (4756819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b82c9255f4ce3761ea28c31e5a78f829497aed8afda0a046a5c824d3457b5`  
		Last Modified: Tue, 01 Nov 2022 19:49:30 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c478cc0a5ed1da94c1f564716ee5f26f416ffb75330a89c1d8ab56b3c42df64`  
		Last Modified: Tue, 01 Nov 2022 19:49:30 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9b5cc15db1001e1f62493bb0f1bbe93104aea8b9faf88bbf46e5ad1cd1500f`  
		Last Modified: Tue, 01 Nov 2022 19:49:30 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; arm variant v6

```console
$ docker pull notary@sha256:f30611ba03f4df33f3965f9c0654aa2e6d64e5ef4463f9c4b15d4e204fb152ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7134833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be94e84004109495197f130d476a33919e4542d156760ac56916805f88e34b15`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 05:30:38 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 05:31:20 GMT
EXPOSE map[4444/tcp:{}]
# Tue, 25 Oct 2022 05:31:20 GMT
EXPOSE map[7899/tcp:{}]
# Tue, 25 Oct 2022 05:31:20 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 25 Oct 2022 05:31:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 25 Oct 2022 05:31:20 GMT
WORKDIR /notary/signer
# Tue, 01 Nov 2022 19:20:26 GMT
COPY /notary-signer ./ # buildkit
# Tue, 01 Nov 2022 19:20:27 GMT
RUN ./notary-signer --version # buildkit
# Tue, 01 Nov 2022 19:20:27 GMT
COPY ./signer-config.json . # buildkit
# Tue, 01 Nov 2022 19:20:27 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 01 Nov 2022 19:20:27 GMT
USER notary
# Tue, 01 Nov 2022 19:20:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:20:27 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719245ee64918db6e14bc8a74787353276669a8486a5743651ec04a1872a4357`  
		Last Modified: Tue, 25 Oct 2022 05:31:43 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d24c426545e5b4d77ea372c858835d4d3cda7f072724f0b6481c74caa9c839d`  
		Last Modified: Tue, 25 Oct 2022 05:31:54 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c617e22eb0af00b379afff9c31ff2f910486d7354d46ff071b4aff16a0e786`  
		Last Modified: Tue, 01 Nov 2022 19:21:00 GMT  
		Size: 4.5 MB (4518731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897a7e7a506d7c5cd85a10f3f2877e0e981d2dba75740529b2da00d5e238341d`  
		Last Modified: Tue, 01 Nov 2022 19:20:59 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76b6966e10c22bb23af0094e4b7ea2aed188334d94989e2cf71fc6bfc6e8c07`  
		Last Modified: Tue, 01 Nov 2022 19:20:59 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0dd830a7fce9f301137087aab9951b337e7e69223eaaf4b288f49c3802e6fc`  
		Last Modified: Tue, 01 Nov 2022 19:20:59 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:e2fed3de49b55e4e02936781f1e37c2e3529125b5d4c5c78d8ffcf125310c475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7093131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110da8136a385e58ac1a4156dc26f7c42cfd365aec60c6d2529443483786a3a9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Thu, 10 Nov 2022 20:39:41 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 05:54:03 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 05:54:20 GMT
EXPOSE map[4444/tcp:{}]
# Tue, 25 Oct 2022 05:54:20 GMT
EXPOSE map[7899/tcp:{}]
# Tue, 25 Oct 2022 05:54:20 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 25 Oct 2022 05:54:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 25 Oct 2022 05:54:20 GMT
WORKDIR /notary/signer
# Thu, 10 Nov 2022 23:37:55 GMT
COPY /notary-signer ./ # buildkit
# Thu, 10 Nov 2022 23:37:56 GMT
RUN ./notary-signer --version # buildkit
# Thu, 10 Nov 2022 23:37:56 GMT
COPY ./signer-config.json . # buildkit
# Thu, 10 Nov 2022 23:37:56 GMT
COPY ./entrypoint.sh . # buildkit
# Thu, 10 Nov 2022 23:37:56 GMT
USER notary
# Thu, 10 Nov 2022 23:37:56 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 10 Nov 2022 23:37:56 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19c11ef8813c7c7e52078792213cc1951b797dfeda0933eb53237672542be0d`  
		Last Modified: Tue, 25 Oct 2022 05:54:34 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bee4f746f272fbd9c98d93ee524cc92d5c98dd19f9296a083af13b222f35c6e`  
		Last Modified: Tue, 25 Oct 2022 05:54:42 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7084a583cc86312f3a1e9663f74ec5e8c5c881f607fe21fada12c2f1812dd5`  
		Last Modified: Thu, 10 Nov 2022 23:38:18 GMT  
		Size: 4.4 MB (4383301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0112b4689d90048ee076e520073cfd8fec2259ba8cc5d55343c777c08aca857`  
		Last Modified: Thu, 10 Nov 2022 23:38:17 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c093f2b008ee0515432e6c9d08176bd1ece16cc8025be1c1b97287c4f89f4`  
		Last Modified: Thu, 10 Nov 2022 23:38:17 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e344dfe31978643ee0e97ac35b2a584e5d08ba81555811d14599eacef223a1`  
		Last Modified: Thu, 10 Nov 2022 23:38:17 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; 386

```console
$ docker pull notary@sha256:7d966fca4f558cc3f76c22132a31c934581ac458df7a21c3ccdbf61a50d134ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7380344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd5a9a2b07ddf37d628def6fcadcab55ad90a20842c5ab2aa645b6314014fbb`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 02:33:41 GMT
RUN adduser -D -H -g "" notary
# Tue, 25 Oct 2022 02:33:59 GMT
EXPOSE 4444
# Tue, 25 Oct 2022 02:34:00 GMT
EXPOSE 7899
# Tue, 25 Oct 2022 02:34:01 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 25 Oct 2022 02:34:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 25 Oct 2022 02:34:03 GMT
WORKDIR /notary/signer
# Tue, 01 Nov 2022 19:10:04 GMT
COPY file:547f217f94a78fab0511c653078b4c2ebbfc2d07327afb125e8459bd4c7bbf8e in ./ 
# Tue, 01 Nov 2022 19:10:04 GMT
RUN ./notary-signer --version
# Tue, 01 Nov 2022 19:10:06 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Tue, 01 Nov 2022 19:10:07 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Tue, 01 Nov 2022 19:10:07 GMT
USER notary
# Tue, 01 Nov 2022 19:10:08 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:10:09 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c692a1d61ff49f4083804ea05880254cdbf59904eff09aa2c9284e77eed914b`  
		Last Modified: Tue, 25 Oct 2022 02:34:26 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edc955b69acafc7ee12b065cf0f66857f32b4058be7283b3be73de602eec02d`  
		Last Modified: Tue, 25 Oct 2022 02:34:38 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14ff1696886fd6061d03a5bdb57d9039d928287616178440f94b8d09d2d8544`  
		Last Modified: Tue, 01 Nov 2022 19:10:39 GMT  
		Size: 4.6 MB (4571178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee33447da80bd71e30b3609b17eafcecc3ed9500b92b3d2fde516262803c5a54`  
		Last Modified: Tue, 01 Nov 2022 19:10:38 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006b26731840b541ad96857c95173596f70177a1a244dbdd0b4849349e0bb1bd`  
		Last Modified: Tue, 01 Nov 2022 19:10:38 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; ppc64le

```console
$ docker pull notary@sha256:c6a444dfd239a960e340701bfad02006b246286c230f2305f6c653ea42464ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7097887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627ee952c5249f8d8440af7d2ab75f474164d0357aea1ad5dc0c9df4463491ea`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 03:23:54 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 03:24:38 GMT
EXPOSE map[4444/tcp:{}]
# Tue, 25 Oct 2022 03:24:38 GMT
EXPOSE map[7899/tcp:{}]
# Tue, 25 Oct 2022 03:24:38 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 25 Oct 2022 03:24:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 25 Oct 2022 03:24:38 GMT
WORKDIR /notary/signer
# Tue, 01 Nov 2022 19:52:59 GMT
COPY /notary-signer ./ # buildkit
# Tue, 01 Nov 2022 19:53:00 GMT
RUN ./notary-signer --version # buildkit
# Tue, 01 Nov 2022 19:53:00 GMT
COPY ./signer-config.json . # buildkit
# Tue, 01 Nov 2022 19:53:00 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 01 Nov 2022 19:53:00 GMT
USER notary
# Tue, 01 Nov 2022 19:53:00 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:53:00 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28847305e982967909062e053ecacc81ae6035a3f7b3587b0e54677ab21f709c`  
		Last Modified: Tue, 25 Oct 2022 03:25:00 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d02c20adc11bb8fb2837a5733cf0aef1f84c4cd0634e062b9104f203e79c46`  
		Last Modified: Tue, 25 Oct 2022 03:25:11 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f2de88dbcf04ce9626c74bafcf97cf45b585dc60e23c85da0409a57bf7d8bc`  
		Last Modified: Tue, 01 Nov 2022 19:53:31 GMT  
		Size: 4.3 MB (4292393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996407ef4d21829dea55dc4f2aa8162cfce33818a0c9568770ceb97b9d3ac303`  
		Last Modified: Tue, 01 Nov 2022 19:53:30 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025a48a658974a1648ca85661e1bb74e0ef407c22407dd5d32af42d44359d2d3`  
		Last Modified: Tue, 01 Nov 2022 19:53:30 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29250b3e8ad80fa14098544518d02759194deb3eb0c2c86f56e46b976b336e06`  
		Last Modified: Tue, 01 Nov 2022 19:53:30 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; s390x

```console
$ docker pull notary@sha256:da5657339d0cfa767bdb2bafa540af9c6b2dd908ce512761028f550dfea5107e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9afafc68a1e4b864e64efa729dbbde167e98e147e5ed1036a065be84a600092`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 01:21:39 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 01:22:14 GMT
EXPOSE map[4444/tcp:{}]
# Tue, 25 Oct 2022 01:22:14 GMT
EXPOSE map[7899/tcp:{}]
# Tue, 25 Oct 2022 01:22:14 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 25 Oct 2022 01:22:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 25 Oct 2022 01:22:14 GMT
WORKDIR /notary/signer
# Tue, 01 Nov 2022 19:23:18 GMT
COPY /notary-signer ./ # buildkit
# Tue, 01 Nov 2022 19:23:18 GMT
RUN ./notary-signer --version # buildkit
# Tue, 01 Nov 2022 19:23:18 GMT
COPY ./signer-config.json . # buildkit
# Tue, 01 Nov 2022 19:23:18 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 01 Nov 2022 19:23:18 GMT
USER notary
# Tue, 01 Nov 2022 19:23:18 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:23:18 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e57b7c2a2dbd108e38c96fd7b110170d3b57a921f34c3b015736a93b17e5ad`  
		Last Modified: Tue, 25 Oct 2022 01:22:34 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc551ab4c025f7c0eea7a8a1e22a13f7c353f3db3a08e4cae43a782e73d9b89a`  
		Last Modified: Tue, 25 Oct 2022 01:22:40 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d777d5c7c7f8c44012da6681277c73552c11a1a8fee1ac2a199efb93ed5f1a`  
		Last Modified: Tue, 01 Nov 2022 19:23:52 GMT  
		Size: 4.6 MB (4601207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a568cfe33412fb2fce4ffe36ec00270e0e9854440486248a43343187b314fe`  
		Last Modified: Tue, 01 Nov 2022 19:23:51 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3544f39b4416a9518311797adda88c8d822f8a0eff90c05508903d230f072aa`  
		Last Modified: Tue, 01 Nov 2022 19:23:51 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c2d2385d5cc36813017f6437df13c00c29a8adf2df304c47091e81e0cbebb9`  
		Last Modified: Tue, 01 Nov 2022 19:23:51 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:signer-0.7.0`

```console
$ docker pull notary@sha256:1f9e1dae375b5a88b60b6904bd6d95a5147df91e119a849a5152002df047a76b
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
$ docker pull notary@sha256:0a2df6aad290e2b26791851f575d7e51364f1b356895234542e5263114dd0e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7565041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7986ccf50366af23344bbe5e5bea20d70224321eab041ce94bbc227fd28d29`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 01:52:21 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 01:52:46 GMT
EXPOSE map[4444/tcp:{}]
# Tue, 25 Oct 2022 01:52:46 GMT
EXPOSE map[7899/tcp:{}]
# Tue, 25 Oct 2022 01:52:46 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 25 Oct 2022 01:52:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 25 Oct 2022 01:52:46 GMT
WORKDIR /notary/signer
# Tue, 01 Nov 2022 19:49:09 GMT
COPY /notary-signer ./ # buildkit
# Tue, 01 Nov 2022 19:49:10 GMT
RUN ./notary-signer --version # buildkit
# Tue, 01 Nov 2022 19:49:10 GMT
COPY ./signer-config.json . # buildkit
# Tue, 01 Nov 2022 19:49:10 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 01 Nov 2022 19:49:10 GMT
USER notary
# Tue, 01 Nov 2022 19:49:10 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:49:10 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ae0db85ee62912972b015b43b47b5849f5b66900a08ad146a42f7c16d02def`  
		Last Modified: Tue, 25 Oct 2022 01:53:00 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc4162474250e31d2a4a4d6cd0a4f0e9813709d78b77293938ace79068cf662`  
		Last Modified: Tue, 25 Oct 2022 01:53:10 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3192cc45dc578f804bb368238b31cd4f7af695d232971b8cec8a96473f753d4`  
		Last Modified: Tue, 01 Nov 2022 19:49:31 GMT  
		Size: 4.8 MB (4756819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b82c9255f4ce3761ea28c31e5a78f829497aed8afda0a046a5c824d3457b5`  
		Last Modified: Tue, 01 Nov 2022 19:49:30 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c478cc0a5ed1da94c1f564716ee5f26f416ffb75330a89c1d8ab56b3c42df64`  
		Last Modified: Tue, 01 Nov 2022 19:49:30 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9b5cc15db1001e1f62493bb0f1bbe93104aea8b9faf88bbf46e5ad1cd1500f`  
		Last Modified: Tue, 01 Nov 2022 19:49:30 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:f30611ba03f4df33f3965f9c0654aa2e6d64e5ef4463f9c4b15d4e204fb152ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7134833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be94e84004109495197f130d476a33919e4542d156760ac56916805f88e34b15`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 05:30:38 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 05:31:20 GMT
EXPOSE map[4444/tcp:{}]
# Tue, 25 Oct 2022 05:31:20 GMT
EXPOSE map[7899/tcp:{}]
# Tue, 25 Oct 2022 05:31:20 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 25 Oct 2022 05:31:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 25 Oct 2022 05:31:20 GMT
WORKDIR /notary/signer
# Tue, 01 Nov 2022 19:20:26 GMT
COPY /notary-signer ./ # buildkit
# Tue, 01 Nov 2022 19:20:27 GMT
RUN ./notary-signer --version # buildkit
# Tue, 01 Nov 2022 19:20:27 GMT
COPY ./signer-config.json . # buildkit
# Tue, 01 Nov 2022 19:20:27 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 01 Nov 2022 19:20:27 GMT
USER notary
# Tue, 01 Nov 2022 19:20:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:20:27 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719245ee64918db6e14bc8a74787353276669a8486a5743651ec04a1872a4357`  
		Last Modified: Tue, 25 Oct 2022 05:31:43 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d24c426545e5b4d77ea372c858835d4d3cda7f072724f0b6481c74caa9c839d`  
		Last Modified: Tue, 25 Oct 2022 05:31:54 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c617e22eb0af00b379afff9c31ff2f910486d7354d46ff071b4aff16a0e786`  
		Last Modified: Tue, 01 Nov 2022 19:21:00 GMT  
		Size: 4.5 MB (4518731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897a7e7a506d7c5cd85a10f3f2877e0e981d2dba75740529b2da00d5e238341d`  
		Last Modified: Tue, 01 Nov 2022 19:20:59 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76b6966e10c22bb23af0094e4b7ea2aed188334d94989e2cf71fc6bfc6e8c07`  
		Last Modified: Tue, 01 Nov 2022 19:20:59 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0dd830a7fce9f301137087aab9951b337e7e69223eaaf4b288f49c3802e6fc`  
		Last Modified: Tue, 01 Nov 2022 19:20:59 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:e2fed3de49b55e4e02936781f1e37c2e3529125b5d4c5c78d8ffcf125310c475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7093131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110da8136a385e58ac1a4156dc26f7c42cfd365aec60c6d2529443483786a3a9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Thu, 10 Nov 2022 20:39:41 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 05:54:03 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 05:54:20 GMT
EXPOSE map[4444/tcp:{}]
# Tue, 25 Oct 2022 05:54:20 GMT
EXPOSE map[7899/tcp:{}]
# Tue, 25 Oct 2022 05:54:20 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 25 Oct 2022 05:54:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 25 Oct 2022 05:54:20 GMT
WORKDIR /notary/signer
# Thu, 10 Nov 2022 23:37:55 GMT
COPY /notary-signer ./ # buildkit
# Thu, 10 Nov 2022 23:37:56 GMT
RUN ./notary-signer --version # buildkit
# Thu, 10 Nov 2022 23:37:56 GMT
COPY ./signer-config.json . # buildkit
# Thu, 10 Nov 2022 23:37:56 GMT
COPY ./entrypoint.sh . # buildkit
# Thu, 10 Nov 2022 23:37:56 GMT
USER notary
# Thu, 10 Nov 2022 23:37:56 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 10 Nov 2022 23:37:56 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19c11ef8813c7c7e52078792213cc1951b797dfeda0933eb53237672542be0d`  
		Last Modified: Tue, 25 Oct 2022 05:54:34 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bee4f746f272fbd9c98d93ee524cc92d5c98dd19f9296a083af13b222f35c6e`  
		Last Modified: Tue, 25 Oct 2022 05:54:42 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7084a583cc86312f3a1e9663f74ec5e8c5c881f607fe21fada12c2f1812dd5`  
		Last Modified: Thu, 10 Nov 2022 23:38:18 GMT  
		Size: 4.4 MB (4383301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0112b4689d90048ee076e520073cfd8fec2259ba8cc5d55343c777c08aca857`  
		Last Modified: Thu, 10 Nov 2022 23:38:17 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c093f2b008ee0515432e6c9d08176bd1ece16cc8025be1c1b97287c4f89f4`  
		Last Modified: Thu, 10 Nov 2022 23:38:17 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e344dfe31978643ee0e97ac35b2a584e5d08ba81555811d14599eacef223a1`  
		Last Modified: Thu, 10 Nov 2022 23:38:17 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:7d966fca4f558cc3f76c22132a31c934581ac458df7a21c3ccdbf61a50d134ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7380344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd5a9a2b07ddf37d628def6fcadcab55ad90a20842c5ab2aa645b6314014fbb`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 02:33:41 GMT
RUN adduser -D -H -g "" notary
# Tue, 25 Oct 2022 02:33:59 GMT
EXPOSE 4444
# Tue, 25 Oct 2022 02:34:00 GMT
EXPOSE 7899
# Tue, 25 Oct 2022 02:34:01 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 25 Oct 2022 02:34:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 25 Oct 2022 02:34:03 GMT
WORKDIR /notary/signer
# Tue, 01 Nov 2022 19:10:04 GMT
COPY file:547f217f94a78fab0511c653078b4c2ebbfc2d07327afb125e8459bd4c7bbf8e in ./ 
# Tue, 01 Nov 2022 19:10:04 GMT
RUN ./notary-signer --version
# Tue, 01 Nov 2022 19:10:06 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Tue, 01 Nov 2022 19:10:07 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Tue, 01 Nov 2022 19:10:07 GMT
USER notary
# Tue, 01 Nov 2022 19:10:08 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:10:09 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c692a1d61ff49f4083804ea05880254cdbf59904eff09aa2c9284e77eed914b`  
		Last Modified: Tue, 25 Oct 2022 02:34:26 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edc955b69acafc7ee12b065cf0f66857f32b4058be7283b3be73de602eec02d`  
		Last Modified: Tue, 25 Oct 2022 02:34:38 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14ff1696886fd6061d03a5bdb57d9039d928287616178440f94b8d09d2d8544`  
		Last Modified: Tue, 01 Nov 2022 19:10:39 GMT  
		Size: 4.6 MB (4571178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee33447da80bd71e30b3609b17eafcecc3ed9500b92b3d2fde516262803c5a54`  
		Last Modified: Tue, 01 Nov 2022 19:10:38 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006b26731840b541ad96857c95173596f70177a1a244dbdd0b4849349e0bb1bd`  
		Last Modified: Tue, 01 Nov 2022 19:10:38 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:c6a444dfd239a960e340701bfad02006b246286c230f2305f6c653ea42464ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7097887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627ee952c5249f8d8440af7d2ab75f474164d0357aea1ad5dc0c9df4463491ea`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 03:23:54 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 03:24:38 GMT
EXPOSE map[4444/tcp:{}]
# Tue, 25 Oct 2022 03:24:38 GMT
EXPOSE map[7899/tcp:{}]
# Tue, 25 Oct 2022 03:24:38 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 25 Oct 2022 03:24:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 25 Oct 2022 03:24:38 GMT
WORKDIR /notary/signer
# Tue, 01 Nov 2022 19:52:59 GMT
COPY /notary-signer ./ # buildkit
# Tue, 01 Nov 2022 19:53:00 GMT
RUN ./notary-signer --version # buildkit
# Tue, 01 Nov 2022 19:53:00 GMT
COPY ./signer-config.json . # buildkit
# Tue, 01 Nov 2022 19:53:00 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 01 Nov 2022 19:53:00 GMT
USER notary
# Tue, 01 Nov 2022 19:53:00 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:53:00 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28847305e982967909062e053ecacc81ae6035a3f7b3587b0e54677ab21f709c`  
		Last Modified: Tue, 25 Oct 2022 03:25:00 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d02c20adc11bb8fb2837a5733cf0aef1f84c4cd0634e062b9104f203e79c46`  
		Last Modified: Tue, 25 Oct 2022 03:25:11 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f2de88dbcf04ce9626c74bafcf97cf45b585dc60e23c85da0409a57bf7d8bc`  
		Last Modified: Tue, 01 Nov 2022 19:53:31 GMT  
		Size: 4.3 MB (4292393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996407ef4d21829dea55dc4f2aa8162cfce33818a0c9568770ceb97b9d3ac303`  
		Last Modified: Tue, 01 Nov 2022 19:53:30 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025a48a658974a1648ca85661e1bb74e0ef407c22407dd5d32af42d44359d2d3`  
		Last Modified: Tue, 01 Nov 2022 19:53:30 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29250b3e8ad80fa14098544518d02759194deb3eb0c2c86f56e46b976b336e06`  
		Last Modified: Tue, 01 Nov 2022 19:53:30 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:da5657339d0cfa767bdb2bafa540af9c6b2dd908ce512761028f550dfea5107e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9afafc68a1e4b864e64efa729dbbde167e98e147e5ed1036a065be84a600092`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 01:21:39 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 01:22:14 GMT
EXPOSE map[4444/tcp:{}]
# Tue, 25 Oct 2022 01:22:14 GMT
EXPOSE map[7899/tcp:{}]
# Tue, 25 Oct 2022 01:22:14 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 25 Oct 2022 01:22:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 25 Oct 2022 01:22:14 GMT
WORKDIR /notary/signer
# Tue, 01 Nov 2022 19:23:18 GMT
COPY /notary-signer ./ # buildkit
# Tue, 01 Nov 2022 19:23:18 GMT
RUN ./notary-signer --version # buildkit
# Tue, 01 Nov 2022 19:23:18 GMT
COPY ./signer-config.json . # buildkit
# Tue, 01 Nov 2022 19:23:18 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 01 Nov 2022 19:23:18 GMT
USER notary
# Tue, 01 Nov 2022 19:23:18 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 01 Nov 2022 19:23:18 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e57b7c2a2dbd108e38c96fd7b110170d3b57a921f34c3b015736a93b17e5ad`  
		Last Modified: Tue, 25 Oct 2022 01:22:34 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc551ab4c025f7c0eea7a8a1e22a13f7c353f3db3a08e4cae43a782e73d9b89a`  
		Last Modified: Tue, 25 Oct 2022 01:22:40 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d777d5c7c7f8c44012da6681277c73552c11a1a8fee1ac2a199efb93ed5f1a`  
		Last Modified: Tue, 01 Nov 2022 19:23:52 GMT  
		Size: 4.6 MB (4601207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a568cfe33412fb2fce4ffe36ec00270e0e9854440486248a43343187b314fe`  
		Last Modified: Tue, 01 Nov 2022 19:23:51 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3544f39b4416a9518311797adda88c8d822f8a0eff90c05508903d230f072aa`  
		Last Modified: Tue, 01 Nov 2022 19:23:51 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c2d2385d5cc36813017f6437df13c00c29a8adf2df304c47091e81e0cbebb9`  
		Last Modified: Tue, 01 Nov 2022 19:23:51 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
