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
