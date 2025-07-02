## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:79e6687b74d38d75b4d93e7e3b7a97487f2331b25ad0abae1d676bae7d7604db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:684140f8d41722bea7cd565b923e1c24a7d6d455417c2e1386947c906612cd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279254966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214d981386f754161074d08bd4b2ad9ef779609fb2971c9ded3117beb6a7b01f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
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
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6730b76d5af51ccc3b319bcab87ceb24db7f72f319da6e8bc117cbd017d79b3c`  
		Last Modified: Wed, 02 Jul 2025 04:17:02 GMT  
		Size: 144.6 MB (144635065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11928356ca6654a55e2221b2d1031c26e478bce83cb2ddde82a1135a687de0a4`  
		Last Modified: Wed, 02 Jul 2025 04:17:37 GMT  
		Size: 85.4 MB (85354987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0020f651b94be401155c14f5dd5da59311c391cabf5e5b59517e3895e483b4`  
		Last Modified: Wed, 02 Jul 2025 04:17:15 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcd7529ab186f1cd5f1b2f4e2036ad5de46e8c67c19c9adc4aa0384e772e07c`  
		Last Modified: Wed, 02 Jul 2025 04:17:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:879284e29ea3d2d13c8d8aded9f95834e9e8037392b444a447cd9f31f8ced04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7474949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c726674346a72ea52d99541faa4f321bfb0d5ff15f04b7981f41494de29bcc78`

```dockerfile
```

-	Layers:
	-	`sha256:4373796a30ee1afeaa0a91826359730b6a051b33ea38cec33c860fef5bf3a7a6`  
		Last Modified: Wed, 02 Jul 2025 06:38:45 GMT  
		Size: 7.5 MB (7459153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d762705ed242442dbbdd811b101692ecd8cbd678cb772faf24ee46b58c3205d`  
		Last Modified: Wed, 02 Jul 2025 06:38:46 GMT  
		Size: 15.8 KB (15796 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:443bb678521b19b1f39b1b792e8d932026d1909fc92bf57983dbb9ecf86757d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 MB (278315944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e345b2f27c0c1d306291acfe6ad94de5fda02fcc794ad8a3a1455417e50a46`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
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
	-	`sha256:2581a046e315a4b3013d50a17da46bcffbba144014a55d733fa55c3bafc6b7ab`  
		Last Modified: Tue, 01 Jul 2025 01:18:05 GMT  
		Size: 49.6 MB (49630154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797600c3e596575d80695bf514135daf4d7943c3274cb76cf5d6b68aaadfa81f`  
		Last Modified: Tue, 01 Jul 2025 12:21:30 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe164e59d1e046ed930f001033c71de0641fd26e8cf8fb58743c067a065ca543`  
		Last Modified: Tue, 01 Jul 2025 12:26:45 GMT  
		Size: 85.2 MB (85172118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb40bf45bad7770767d93bf1140f2809b966ec9d5fe76b6077e80e94244bfbf9`  
		Last Modified: Tue, 01 Jul 2025 12:26:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31322016dcf51a81c50a4031b219ca000b3e2fc3c1397cf26a5d051716087df4`  
		Last Modified: Tue, 01 Jul 2025 12:26:39 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9817ab91b0994c382e13c86f66d8f26b19da39f4eb8177cafa285495b4cad946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dea3003a11c934af3706d5f36bcec4c70eb2a3bce870e880fd89ea284035c0b`

```dockerfile
```

-	Layers:
	-	`sha256:d2a9d4321eb20a35a8431cc898cf90c8b13ffab30990cc0650c0e4ceea56b2d0`  
		Last Modified: Tue, 01 Jul 2025 15:37:54 GMT  
		Size: 7.5 MB (7466183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3dd9058fa4ee1300223ac88442abc93bafcf721fa6d6385be58a34d4eb8f615`  
		Last Modified: Tue, 01 Jul 2025 15:37:55 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:93e1583c11086ca77a20d77c926704247b63a51bf222175c2e29b6d26bb0994a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288148271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771cade0c320efa51bcdb426b565fec620c8cce95ea88a893eca8b80792fc6cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
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
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0584037f9e2e942ab798efa93b8fd502cab7aa17a73e78e986f82b3b700b3380`  
		Last Modified: Tue, 01 Jul 2025 13:31:59 GMT  
		Size: 144.3 MB (144280582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaede1bfe2e32ffbc526cbdf924b2502c82c8cb59d870ba8a001e976f7c08309`  
		Last Modified: Tue, 01 Jul 2025 08:53:03 GMT  
		Size: 90.8 MB (90769413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e56d0b2542b9f41cc93f382cac156a78db2fad88bfb87d2d53b6b8300cd28dc`  
		Last Modified: Tue, 01 Jul 2025 08:52:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6b31fc82229162a92f998e0ec7d473e8b41d1cb6995544bca522d782bf2c62`  
		Last Modified: Tue, 01 Jul 2025 08:52:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9994b0322d1e63b2602d3a7446572ea55c41e129e66278a50d64a5eaf6ba2bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128a7f06295afafddbab9832ea62e771bf3c0421c7009899b199c9d75bf6e8b3`

```dockerfile
```

-	Layers:
	-	`sha256:fd1e3c037e7e9afa15b9c80484de506c0bce2ac889e5c2107bf24ff0e0230208`  
		Last Modified: Tue, 01 Jul 2025 09:38:35 GMT  
		Size: 7.5 MB (7463570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0829e974bef2f4f683ce6b86cfb2d7b0ef7379faaf9a447928d6ee0bf480a3c4`  
		Last Modified: Tue, 01 Jul 2025 09:38:36 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:90f64b81769801bbb660b1116f144927357767630eaf5149089b076eef2a0989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270481911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e409f4b4ed849fff5b74f5efe3d1884d9853b808592401b59ac62840ebf7679d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
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
	-	`sha256:a19cda6d0aca0ae93b23898ddaa4518ab5077c7011f945c7a7e4a2cacb08ca5f`  
		Last Modified: Tue, 01 Jul 2025 01:23:18 GMT  
		Size: 47.8 MB (47750158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3e53d716a4eca82bc7ec1d014b1e63164f7a508de7049dd71a1355386dbfc`  
		Last Modified: Tue, 01 Jul 2025 02:33:31 GMT  
		Size: 138.5 MB (138492488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c63f0c5a295ac31376dfa16adc9e52085a21d933a7ee3057a9cf5207e485c1f`  
		Last Modified: Tue, 01 Jul 2025 02:48:27 GMT  
		Size: 84.2 MB (84238222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cce080ac0586c0d8a8d288fedf5b576c87ec98c60f5bd04c60cd2620f5a362`  
		Last Modified: Tue, 01 Jul 2025 02:48:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655234db54803e4e863eb472cfdfc42ca1f87448c021a84fdee2b89d2653dec4`  
		Last Modified: Tue, 01 Jul 2025 02:48:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:59f6cce5e6ca680eda03598ddf0d278c229cd8c3bef054c7c878febed1d6e190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7460990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ea15d53f500595cda1dfeae68d8e3e9b7abc842928f94d7b459173dc4debda`

```dockerfile
```

-	Layers:
	-	`sha256:dc9efc3133f6ad6d915cd22aae5e1c9e63380fd79e7143adb9adeced1785089c`  
		Last Modified: Tue, 01 Jul 2025 03:36:19 GMT  
		Size: 7.4 MB (7445145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f305567feb76fcbe18d6a5c5b50db788bc755ad1c1141caa36665ca262deeaf`  
		Last Modified: Tue, 01 Jul 2025 03:36:20 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:1bfdb505006ed832fce8f840848bf5fa466bc6b7ce1432756182aef499bcd9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270352330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cf72d148228a5acf67eb8cdfd17ea910dac2cf193409b22b51a79d16c8b23d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
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
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968c8d7f32961543a7f872e2e66912ec4216d7c221769ba446e70bd47f4dafa6`  
		Last Modified: Tue, 01 Jul 2025 13:32:01 GMT  
		Size: 134.7 MB (134673550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272e96b0a5da4720e4a4eab688bd5f2c390b8c0fe3e81cb777de890417c430c6`  
		Last Modified: Tue, 01 Jul 2025 08:15:47 GMT  
		Size: 86.3 MB (86334079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52f27eb0cb63d5e1cad76aa3c817b108906a0701e14854a6cbf6e0fd5e5a962`  
		Last Modified: Tue, 01 Jul 2025 08:15:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d369a35c5419fb0642d1838ee7de46fa81497a1c7b211ff9aa337c2220e2445`  
		Last Modified: Tue, 01 Jul 2025 08:15:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8886d32859bbd2168131f844474dc8f3e323746860b2874d71702ad1eedae0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7470872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93407c8dffa6aa471182dd65310b6160b53f350934f1711c38414fbcffb0782e`

```dockerfile
```

-	Layers:
	-	`sha256:d0132535b7576064446940a2d0cc22c13484dedf47e18ef1824db8a508a1f60a`  
		Last Modified: Tue, 01 Jul 2025 09:38:45 GMT  
		Size: 7.5 MB (7455075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fed693e5b069282a9f548760cdb00ac1cad3139bb0b4f5450526a2e27842caa`  
		Last Modified: Tue, 01 Jul 2025 09:38:46 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
