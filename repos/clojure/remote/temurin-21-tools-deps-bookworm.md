## `clojure:temurin-21-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:bc70047add2c76f32bf52f55f434ed108093a9370f4526afdb297f32497f4047
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

### `clojure:temurin-21-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:535a2ee79cf0eb612a07efdbf2208ada4f16eb1def927e447c09a243048bea08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287459275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a910268e4f409c259ead41b601d81a14813b7a779d8ee497757930038e20c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:05:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:05:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:05:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:05:28 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:05:28 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:05:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:05:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:05:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:05:48 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:05:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21926b973db02b21073b36d8cd982282fb87eef9b7186aca51cad66921b706e2`  
		Last Modified: Wed, 28 Jan 2026 18:06:13 GMT  
		Size: 157.8 MB (157826006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f84df5e7eec81d11fc2c98afbcab495f96ffe76780383c1c5d7897078bb0294`  
		Last Modified: Wed, 28 Jan 2026 18:06:11 GMT  
		Size: 81.2 MB (81150606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff5c837df09aab0e2342d87b4f23c5dcc79f8d17dafbf3fe490c4ea5c1636ed`  
		Last Modified: Wed, 28 Jan 2026 18:06:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0b2d582b64a201f0d72be7c8c1fd3b891012d6a72a1bee47fcda9f8728030c`  
		Last Modified: Wed, 28 Jan 2026 18:06:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:98a277b31416771fa8f42905a889cb91bc255957ae27952bc234fa5a5ebd4060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6e1609819f315b15ae961bbf952794fc90504039cff30925db056cee50646c`

```dockerfile
```

-	Layers:
	-	`sha256:c3ced146eb84be54100430e63f26a549740691a6687351e57b7aa50ee52452f4`  
		Last Modified: Wed, 28 Jan 2026 18:06:08 GMT  
		Size: 7.4 MB (7379323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edb087cbf75b232cbe9f79fa8d511b0a1699d7d10228e46ff2fd0bd702bb6b93`  
		Last Modified: Wed, 28 Jan 2026 18:06:08 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b45288eea0ff7efa0cfa215c1164b31351543577e09cd2b05c84c62b78aba7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.6 MB (285613019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1ec7f5fa892240abebdd402812ed60df2aa34ef37663b82dd85b67936b721a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:04:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:04:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:04:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:04:51 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:04:51 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:05:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:05:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:05:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:05:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:05:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9c25cd62af5fe4e3758adf6264e69fe8f584b3084938bd39da9e6d751b8391`  
		Last Modified: Wed, 28 Jan 2026 18:05:36 GMT  
		Size: 156.1 MB (156107578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26991754b72d89ba0dc792af4649abac618e093b56747b492b75527fd1312df`  
		Last Modified: Wed, 28 Jan 2026 18:05:30 GMT  
		Size: 81.1 MB (81138324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cefc45326152be6e6bb6d43b73694c90bc4ff16cf2604ef955e873877b4134`  
		Last Modified: Wed, 28 Jan 2026 18:05:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57b3ed1665a33ab53799b26494920035e0f6a8a387b7dd51b056a9719ca41a7`  
		Last Modified: Wed, 28 Jan 2026 18:05:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:facefc5ddacd46cba6db7938d2d60ab3f747796ac9c6a3e997a4e9443e3b8108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205a1bd81c5647271ad1d44c93ccc7a9bffa47ed165196b82a589b8cbf9d0403`

```dockerfile
```

-	Layers:
	-	`sha256:f9c5e38d875459ae913f2a4786217ed261e7083c6107506eb8fedcaf584e7972`  
		Last Modified: Wed, 28 Jan 2026 18:05:27 GMT  
		Size: 7.4 MB (7385110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efbd900ed2f6ceb17c345603a6ec20d13aa95142220613fe3f239d8803b4683d`  
		Last Modified: Wed, 28 Jan 2026 18:05:27 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:31d938a04798d7e3509b5153420c4129103e89a8d67609b21ebda91630dd0e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297258437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb295ac0e57f81e6f4024f96611789ff29029e6e892008430bcc955d805b841`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:26:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:26:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:26:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:26:59 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:26:59 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:27:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:27:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:27:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:27:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:27:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3edee8149cf4bfe2bdf95487958a292e196ba2b723670ee4a4e1e494c9284d`  
		Last Modified: Wed, 28 Jan 2026 18:28:23 GMT  
		Size: 157.9 MB (157942968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5decf3715d411e1228584850542c13f35f5582886cf3a94dbe596cc00fc1c246`  
		Last Modified: Wed, 28 Jan 2026 18:28:21 GMT  
		Size: 87.0 MB (86987051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041a0e0383c89680541621dc49121ebaf534665605dcf970acee7c6d2d831d5d`  
		Last Modified: Wed, 28 Jan 2026 18:28:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21076fd1d5d115e3306a497932f5a32f591ac9b742a13c84649fe33d9f0c7dac`  
		Last Modified: Wed, 28 Jan 2026 18:28:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fff281492b10043707927c233f36d2606debbda428f0b0f267e9af39117e7172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca49ad3dc566d16cb815e9aefbcc1be1c34f95098ff6abbb047d94088134d499`

```dockerfile
```

-	Layers:
	-	`sha256:a514158a289df9f2bb370d31edfa4af31c890ad6d0cd6ee145269a6805647c2c`  
		Last Modified: Wed, 28 Jan 2026 18:28:18 GMT  
		Size: 7.4 MB (7384551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9de96522f39f12e6ab6d0a412d8acfee513dc45f3f37284cb385275175185603`  
		Last Modified: Wed, 28 Jan 2026 18:28:17 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:b2ba01b02c652d20a64a8b0ca1aff9975428c0b24ed591958561fe04c6941e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274172678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27513a2962eda35fbeef0b231d1297fedc9c2ed58c56e84da081e9adb65360a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:19:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:19:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:19:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:19:49 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 15 Jan 2026 23:19:49 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:10:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:10:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:10:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:10:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:10:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:05 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870218276608e18166550d6fb6c5680cebf5e7e53f9ed38d4773065c75b378a`  
		Last Modified: Thu, 15 Jan 2026 23:20:38 GMT  
		Size: 147.1 MB (147069856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736366fd96cfcf1514e65546d3a005d424606f9bd6d359c54f0a74d2cee3c71f`  
		Last Modified: Wed, 28 Jan 2026 18:11:08 GMT  
		Size: 80.0 MB (79963350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf3bc470f15cb61e401b18580e0065433f86db9a74f8ee692a7f8e9a51a48b2`  
		Last Modified: Wed, 28 Jan 2026 18:11:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb99211d75dd45f0621b332c62dce59305d95a0760d80a312069b8a4f2db9fe2`  
		Last Modified: Wed, 28 Jan 2026 18:11:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ac54b9dab093859e43bb024ee5370ae3c3df996e93efd9a4f84b2f3c5ad542b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7387104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88e14df2b21b1a72e14917f63c86f6263ba50d7ac278c4d1dd935a23dba5b73`

```dockerfile
```

-	Layers:
	-	`sha256:15b4592092a5489443802ed31175d35241be599364c8f9ed9fa8e95f174084bf`  
		Last Modified: Wed, 28 Jan 2026 18:11:06 GMT  
		Size: 7.4 MB (7370642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f0d000308cba4a36ae730bcd7ff8309c93ad48e68e0a91726b6a636116eaa06`  
		Last Modified: Wed, 28 Jan 2026 18:11:06 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
