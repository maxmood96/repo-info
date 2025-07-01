## `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm`

```console
$ docker pull clojure@sha256:941353dec21c20f7194a7db10d90773960115c3df4774d3c8c01526864f85226
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:0d43614b74e291acd77c5f705ffe27a923adf56f5f190f2bf513af35966a366a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219440337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ec2129543aefa0d72f1d7e8f715e2b10e077d2ad6fa35e97f5fefd9528b95e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e264ceac2c88e848475a7ba102a67f9179f454db8cd7506423f58360698d7c1`  
		Last Modified: Tue, 01 Jul 2025 02:40:49 GMT  
		Size: 90.0 MB (89952004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7824768488fac23490221a185a8cf6d8ea98b5185df6c7039ed3eb4e2196896`  
		Last Modified: Tue, 01 Jul 2025 02:40:49 GMT  
		Size: 81.0 MB (80993007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4ba3f2478e12e3c0bb71fb05f616920c20390345be64370a6b2fd9b6238363`  
		Last Modified: Tue, 01 Jul 2025 02:40:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953198c000c8ca56e85e02e04dd54b92709defbac08c39fc5e2ce81c95b66376`  
		Last Modified: Tue, 01 Jul 2025 02:40:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:138bddfe0b6e34349942b38126ea397e1d81285c9544024d11abac8acb63df8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7336095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add2ce68570952a44dd77fb6a4f795ad9572b0c7373e47692ff1a2938f9606b0`

```dockerfile
```

-	Layers:
	-	`sha256:c4a6d548835b6f2a0ec44af57bffaf755aa7a3113cc5f187d3198829a928ea03`  
		Last Modified: Tue, 01 Jul 2025 06:40:14 GMT  
		Size: 7.3 MB (7319598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7624ffc804011366a504af1636967ef4bbf7c2e590e685fa849b9c9b05daaa55`  
		Last Modified: Tue, 01 Jul 2025 06:40:15 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:716da25deee2fc9bbdb5239c4805a202b96f92997cbd3523e55e80d8c360fbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218279427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30dc716d7b3ac5ef90858de785efb1de8db34d66b39eddba233d120e9d8414d7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab3c421cf8efb93f9d89023e10eb881af74b9179f55fc8b660865f6d98c99f7`  
		Last Modified: Wed, 11 Jun 2025 08:42:55 GMT  
		Size: 89.1 MB (89091275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9460f751fb6b257e538f4ab00ed9fd4f5fc5e3e441cb1d46fdf1b4ea3ddbdab`  
		Last Modified: Wed, 11 Jun 2025 08:47:28 GMT  
		Size: 80.8 MB (80848263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219f5d922bd6cd71c13d79f95000f6c5d6f841a833695e5787231721a3dafd9a`  
		Last Modified: Wed, 11 Jun 2025 08:46:52 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80eb17adca0fc78ba366b9f007579472def8b1bcf425f0e70d3a722373c2effa`  
		Last Modified: Wed, 11 Jun 2025 08:46:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a210bc8119c3803a941ae985b5fb706ee1eb19e40f12fa2410a59d37960ccec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7340665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19b7120fc49760140f72eb72359aeb132f7a34c2552969e6543b64844457f6b`

```dockerfile
```

-	Layers:
	-	`sha256:91a91f47ff7f6a2cc571f2d4887833747df378159ca4f847cf862829c3c23d06`  
		Last Modified: Wed, 11 Jun 2025 09:40:48 GMT  
		Size: 7.3 MB (7324026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:856eed2efb4d5fe8c9eab8e1b968317503a593e4c97d9a1184d9f5dbfd25d450`  
		Last Modified: Wed, 11 Jun 2025 09:40:49 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:9fdb869e6b32888f81a3ccd61878d28cc255fc883515584e340e23eb1425a10e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229072075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0038e337c9d40f2d4a6c0f91d3b07212480032fe8961e02bb949f0b35878509b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ea6852e3db17e417a9170041e86c2edb5e1fc589eb78623a2d1e2764bb35d2`  
		Last Modified: Wed, 11 Jun 2025 08:52:17 GMT  
		Size: 89.9 MB (89920274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eae927425e25f4dbdd4e9108acfed83eeee607b1c3ec4bace680a791b0e10c1`  
		Last Modified: Wed, 11 Jun 2025 08:59:01 GMT  
		Size: 86.8 MB (86813401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b528f2cccdc00c2c606f60c6aadeb1f513fcfdf0c0077a2b4dd198f61a8263`  
		Last Modified: Wed, 11 Jun 2025 08:58:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da5fd56fb0a791c9190c1a58da015ff90271f5ec70c6b3d3e28723f1d0d6a7`  
		Last Modified: Wed, 11 Jun 2025 08:58:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1beb6ded04d9c92180e9da572c41cfe848e451e4ee775ad429906a5fdb5b037d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4fd00188f3c318ea3199c8270eef207c3d60a556a3a0560c7ffdee3085948d`

```dockerfile
```

-	Layers:
	-	`sha256:177764f8fb5c404c13c18c5183d6e0445f8392026faba4fc6c55baf0f7a712bb`  
		Last Modified: Wed, 11 Jun 2025 09:40:54 GMT  
		Size: 7.3 MB (7324756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42d66535b65832fd76b74b86b1df4946286c2093041db3c37543c5eeddcacc5a`  
		Last Modified: Wed, 11 Jun 2025 09:40:55 GMT  
		Size: 16.6 KB (16558 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:8acdae33d772fd99fd36279aec5bbef3211bb1d377e37b1af2122fea8f6b48a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212169686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4ae86eaec6c5b377715a69ecca911f087ba34ea8cf2657ca90aba9d4a7361e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:92d876c60c42d9677caf30587cba2266fe6860ddc50efdd0a6fcec154e589f76`  
		Last Modified: Tue, 10 Jun 2025 22:48:13 GMT  
		Size: 47.1 MB (47149408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4e5322a855998805791838cb1c0a7133ae522cc712e1f6b1a57c821a987081`  
		Last Modified: Wed, 11 Jun 2025 12:07:22 GMT  
		Size: 85.2 MB (85216766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adefe3a62e11c9c96f804861eb89533522f46b38640f816800d0f45e0557b973`  
		Last Modified: Wed, 11 Jun 2025 06:02:13 GMT  
		Size: 79.8 MB (79802473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf261ead6c5137b0f5bf8c586f62cbd587d4646cff7c42f7c8813bf771755d9`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46bd954e68e042a4767f7da66b5dc13cd0eb94a2b74e1b11066c9f925f8ffde`  
		Last Modified: Wed, 11 Jun 2025 06:07:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d6bb872e7899f12f4c04e0e38dc0e3e87c369f02a663ebbe07576b7634078ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7328607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7591b6278d21cab7eb33bffbbf82ee7f289ad7fb3cbbeafb6c34810b10bbd623`

```dockerfile
```

-	Layers:
	-	`sha256:2a8fef4b2b5d8a225d145faa5a2b475bbaaa3ce551ada5373d756ed0d6c228d6`  
		Last Modified: Wed, 11 Jun 2025 06:38:50 GMT  
		Size: 7.3 MB (7312109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a032c27fe180028214dd13e4c354b1a0acafa8dc708b05de49b8824c98dc0a3`  
		Last Modified: Wed, 11 Jun 2025 06:38:51 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json
