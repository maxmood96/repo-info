## `notary:signer-0.7.0`

```console
$ docker pull notary@sha256:e7acfa6643735fbc067b639d24e6a2acbd4985e30e90e1ab8dd940b7002583db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `notary:signer-0.7.0` - linux; amd64

```console
$ docker pull notary@sha256:a5f3cf14ec1f9dbe64f5038168764468bf8cf36023f8c1d763abd3bcbe2a5952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7572933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61447c100d57a41cd6d7de0b918e258904d083cab09c7b290a8e5cddf1a383a4`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0a66a0a7b087da7f9fa9bcdc96d80ae3321e565fc4a638465abdeb792ea1ab`  
		Last Modified: Fri, 01 Dec 2023 00:11:09 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f52aecd80f774b20144d76df7a1bd30afde4c022a082345e77412724e5de78d`  
		Last Modified: Fri, 01 Dec 2023 00:11:09 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8e5637f614944c20b445d103b62cbf9d5075cffbc97f04ac7e7934dccdcfde`  
		Last Modified: Fri, 01 Dec 2023 00:11:09 GMT  
		Size: 4.8 MB (4763081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6da303ea01f1dcceeed1c542f07d37db7d2365b66f40e36af725411bb4f125`  
		Last Modified: Fri, 01 Dec 2023 00:11:10 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b01e3f98461ce88ec08bac5847e6bee5cab2727f844407e5ffb58c77e9a1ac6`  
		Last Modified: Fri, 01 Dec 2023 00:11:10 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:9346c6fe8bf3d29a34e0e1d10f1730feff4461a2e4e2cec704a90490be890d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 KB (107256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64d8edc2c7e9d523a11d6b1ea4764f09f5f5fc6fe7551968068c4294c1c0f48`

```dockerfile
```

-	Layers:
	-	`sha256:f05c794c11c4670ee3b2bf18f481970753817e33407b854e72b92746a6734dee`  
		Last Modified: Fri, 01 Dec 2023 00:11:09 GMT  
		Size: 88.0 KB (88011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:080d7a72705ea449c50069d2ca075026c7cfb046eed5d6d3923af5215bc7dbca`  
		Last Modified: Fri, 01 Dec 2023 00:11:09 GMT  
		Size: 19.2 KB (19245 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:5fdb9009bee2a9102d0fd29a4113f4c29cc9b74d654186e4e13ffcecbc722e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aec235975a04dc5580e5f759fa174a5efd4d835df2818c236805808532a5f9b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:321b24cc0fbd39caa2d7672a740d2cd2030ba99cab16f50c22db9955bd99350b in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:dffa980f71c953938bb194a457aa62e7f1885137331eef8bf7f9403c075f711c`  
		Last Modified: Mon, 07 Aug 2023 19:50:02 GMT  
		Size: 2.6 MB (2615553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253ae7f8eb52a8ea4fe35dad1a51da8e2507ed4a7de0e040345c7f1778fa3728`  
		Last Modified: Mon, 07 Aug 2023 22:58:38 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe858dda9ac67d7da225bf0e7cbb97c3d8168347d4bdd73f887f4add26a7e7e3`  
		Last Modified: Mon, 07 Aug 2023 22:58:59 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbc8c04719ae3263711caaa86e777271ef591ecad80813f9fafeae903fd0db3`  
		Last Modified: Mon, 07 Aug 2023 22:59:00 GMT  
		Size: 4.5 MB (4526096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0fc61eff27830763478c3589a62d809f4e27a7f2767f8740c55c4f92be583c`  
		Last Modified: Mon, 07 Aug 2023 22:58:59 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609ae2997199f3151e09c1705027e568d72f65008e6466cc501661f3e76cd7ca`  
		Last Modified: Mon, 07 Aug 2023 22:58:59 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:d0b2157e191e4ba482b1840f736d0d5f8e03e69cd939e2997b53bf9bb70cb016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7103175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69eec41fd3d6cf59d8bb581a10497f7417bffab2b543059ee887a590df99b84`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202c4dd0f102d31afdf745598c8b608887eb3b4142b5fbb8619d8b431ab3d348`  
		Last Modified: Mon, 07 Aug 2023 22:45:27 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f88739c04bec4884bc40c7d216e4e9211441e2d033c5861f631bb0925b478fa`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 118.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f13b4a5fcaf14870b0afd1801c5ea0380125660000fd5e65bc19c7ae8dee6d`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 4.4 MB (4393084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b200dfa82abb58b4aa87e1cda3b731e8020c5ca1217d041b2c3c0284514c9c4`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da7244fcfdb45e21dcac9ea3d397ec3d43317799fbc86f16ec39bc6827ade69`  
		Last Modified: Mon, 07 Aug 2023 22:45:46 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:244799276b035bce3224f3f79c4b7b9e0aded1870794878003a52a9d8cf3781a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 KB (106071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afda2c6f5dcb6f88ab10fcb1bcd90bd754e6d4d6b6edb0dfa41e75749e23832c`

```dockerfile
```

-	Layers:
	-	`sha256:7c9c855ac1ab70995fcbf9fe9684adc44c7aa1c882133bf2d8dc85721cb2d860`  
		Last Modified: Tue, 17 Oct 2023 19:00:44 GMT  
		Size: 87.6 KB (87640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdca200e6121df920c204dc77a79b981b9384195ab438933a829f9c1d6ab18ca`  
		Last Modified: Tue, 17 Oct 2023 19:00:45 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:c3c9cfa8a3e89ea14663516300287f199daaed5aef0c6a0063ba451673d9c085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d486e4ae2bb3d2cab2dde433f02130da8ae238b161d56700c17325b5e77093`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:c06b4f6991638e506d4d0a4d70c4a78ba30b971767802af4c6b837cdf59d4303 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:be0d19c155de823c6b37eaaba7cdec9085e8f1e39b1dd5982a19acb6c8c97cc5`  
		Last Modified: Mon, 07 Aug 2023 19:39:20 GMT  
		Size: 2.8 MB (2810553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596da12c2e0de93c921f09f80dc157315fd51dc526c26c681e009068df5568c8`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bb43db3153fdcdf459b45889c76eeaca751b5a0febc7091e481cba1037f6eb`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b757696a027c52ff6a4f41267a37af932d79007fe75adef68a03e4db29cab75b`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 4.6 MB (4579028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9801338c9c3995199351989ccf7a80c57e88a1a2ba79e8b71870abe62355662c`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e6f75c5fee4e0b872d36961655c4e8103de49fe771f2390af597ea1dc591bf`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:2a7832d044b996c0336436dcdb25e356d5267cb1be5438344c16b4f1368a55a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2c1e17b9b29692bdea190cc1626243bc46b522299047c6b7ec5a764c5f987e`

```dockerfile
```

-	Layers:
	-	`sha256:eae9624154b2c579a780e1c33f1d0df3e69761a24ad7d3414c420d01c825a058`  
		Last Modified: Tue, 17 Oct 2023 18:59:50 GMT  
		Size: 19.0 KB (19002 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:8e2d7e9e0b6f610e145fe2763452f0fa6bf2753d2ea1fad370b3bcc10a0c4f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7101376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4371a66e28772fd7bd0f365e7c22523f8110639edde31c01d2e15b05b73380a9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:b30c2945bf4c873440b2e390c7120f16abe08ec41b10c2fb248b9b1a7ad223fa in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:cc1a557f8d111cc8c11359cd168abb441e150c9dc42a046349c5e51132461a47`  
		Last Modified: Mon, 07 Aug 2023 20:17:53 GMT  
		Size: 2.8 MB (2802326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4d9f67868be443e2c2f090de7caea30272fbfa297b89c353c3ad9a3047b1b6`  
		Last Modified: Tue, 08 Aug 2023 01:08:52 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6bd11e750564a61a33996fb08fc38ada593f7823ecaccb23125be14e4bf09f`  
		Last Modified: Tue, 08 Aug 2023 01:39:25 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c573b997a055b49ebb28df708ccd35e322e96c34fbd6fe31b349be82ceb426`  
		Last Modified: Tue, 08 Aug 2023 01:39:26 GMT  
		Size: 4.3 MB (4296977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31213f0f3061baad77fce782c27b0f9752d96d5efb9d05256f12d3b867d6a009`  
		Last Modified: Tue, 08 Aug 2023 01:39:26 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05359a8b732c0eabd34a61042fbb4826c60251cd3227746cf8ac7ef7ff2f411d`  
		Last Modified: Tue, 08 Aug 2023 01:39:26 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:d3d7190db2f83a210a8559277202cc4dcf9c76305df8e21458952d6c72ad9be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 KB (104194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a22736f296a7310d9e88c5edd6f468643dc37229936c46ccb16031a73732bd4`

```dockerfile
```

-	Layers:
	-	`sha256:09d5296d0c2dd552a8adf45054c19cb0fea69c2a00fe605e3a85029f178be726`  
		Last Modified: Tue, 17 Oct 2023 19:00:34 GMT  
		Size: 85.7 KB (85733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e6efb4b9b3b3f23f45da85a4bb8f418f946bacb09e64a5d4c7c797fc78f9f94`  
		Last Modified: Tue, 17 Oct 2023 19:00:34 GMT  
		Size: 18.5 KB (18461 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:319f21d2ddd35d20943a31dded0fad5d24a3afb0985abfa0a709c8e676a772f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421fdca38a4b1ebe2321e27db10001ec12a1597aa5b5f378a76b284e96d0513c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:39bfe995aa06bc953f4887751caefaa4576f3dfe63f0020b8989bb8b0a09c28f in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:e5761c1ed80af1ea48f655cdeb0fa9a89fe7d3903985d9ea08286e940a4f30dd`  
		Last Modified: Mon, 07 Aug 2023 19:42:55 GMT  
		Size: 2.6 MB (2591728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f55e3cbca2287bf936764f7cf3d3b0b4e12e954928cb0652b427c0f83cf162c`  
		Last Modified: Tue, 08 Aug 2023 05:26:46 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0675d7212e30a1beebba53fe2bb273bb1b10a0a3bfecec0797d9f9f49f235635`  
		Last Modified: Tue, 08 Aug 2023 05:30:24 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e10cf9585fd55e6c66f374ba49ab100672415130008c82ab7e57f9e9546e044`  
		Last Modified: Tue, 08 Aug 2023 05:30:25 GMT  
		Size: 4.6 MB (4606700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950ca5e57e3b0a0e35bf3b1b98dc81ee770fef5cea6b1d28c9c3e3684817c80b`  
		Last Modified: Tue, 08 Aug 2023 05:30:24 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91afc82a44ac77e18bcdebfc2c102118f68cb968b983168e0eaada234ddf83e1`  
		Last Modified: Tue, 08 Aug 2023 05:30:24 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:6628eb1cddc7f1bd905495ac37e84a7518debc0599eea48cddcfecbe477c0c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 KB (104124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c79c56ed31abb498e5552206aa57e05b0c864a1334d5fdf3bba682e27ac6d37`

```dockerfile
```

-	Layers:
	-	`sha256:e409f2918115f3f12c2329e8e6093a4ed211eddd351d22233cfc88a2cefacbd4`  
		Last Modified: Tue, 17 Oct 2023 18:59:42 GMT  
		Size: 85.7 KB (85699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b57d4dde9918e9e768ee93a2ac1cb2d827f413599626be54ac16d9c29e063e59`  
		Last Modified: Tue, 17 Oct 2023 18:59:42 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json
