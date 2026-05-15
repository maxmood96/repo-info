## `clojure:temurin-25-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:2d71198afa8e0e34a31e99218176a4a973878ca02948be3cff6aa71db45d7253
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

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6a78b84ea278af9037b3e4f061e5fcfe76cdab4cd3942a039f90a761363ac42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194402354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4729f9c319f984f06d0c0b9b605c80cb0324fc996b9e96cd98d8bdcf78a2db63`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:36:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:39 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:39 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:54 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc00d5c44ca601ed66cced999a54911bcb4266aa4258953c583c1621142f2af`  
		Last Modified: Thu, 14 May 2026 23:37:13 GMT  
		Size: 92.6 MB (92574586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6231889addb24cdd49b2ecee996649af7e2ae547bd446acda2d248a1007821c4`  
		Last Modified: Thu, 14 May 2026 23:37:13 GMT  
		Size: 72.0 MB (72046500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684f21ca6520f1341c991b411dced0624ea9e3a2f5e55bcf1a36bc1bda64ae02`  
		Last Modified: Thu, 14 May 2026 23:37:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd604344a2ddc9e29eb6300943d69747e5caae7adfb28445f67122cf754586b`  
		Last Modified: Thu, 14 May 2026 23:37:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b0d7e00e861db559a706e8989f010ff3e5cef58e7eb394197945f8d343c88c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5244581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b72655871599d7307a75e68ea374eba4162c98a32dbb2abe8c73613311ddd2`

```dockerfile
```

-	Layers:
	-	`sha256:20ff7488769c3bb19a27ab001f665d5feaea6f9b38eb92dda5e6e2b586816be9`  
		Last Modified: Thu, 14 May 2026 23:37:10 GMT  
		Size: 5.2 MB (5227935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f5654ab2ff145066248256639f279dff32a584b34a5337f061aa273c0fe9a89`  
		Last Modified: Thu, 14 May 2026 23:37:10 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:723ed8bb545ecdbfafdca76089bbb4d0b30d28fba00af5e7957b00602b2735fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193541572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522fa5d54015a4c9aebc1a7a1b6d6337278cdf5861a5ebd2c9cdcd755caadc8c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:36:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:41 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:41 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:58 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca55ba259ca714b005e188cd69078e78b3d840f618777af902a565d752594061`  
		Last Modified: Thu, 14 May 2026 23:37:19 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58025931d8fe6c8e91afd1cc990e2a92208f20551764ba44689d38a3379b20db`  
		Last Modified: Thu, 14 May 2026 23:37:19 GMT  
		Size: 71.9 MB (71854635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bcc35f2ebe7d851319f3fc3b15374463df1bda62563b33f0ef4670923c9bd3`  
		Last Modified: Thu, 14 May 2026 23:37:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696fe2e72a4ac1f6f34762e3fe037ecaf9daaae3256727cc4289e50a1c45c495`  
		Last Modified: Thu, 14 May 2026 23:37:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:de5e2124b1405af7156ed87a0c3eef0e00016dedefaa0dc194186dadd01d42a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5250514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390c818c67d2c78e7ca68896ec97523edbc03c5de124872458a6a9beff1793cb`

```dockerfile
```

-	Layers:
	-	`sha256:4f48f02a0951b1c6e77244e1946f89d5217594cd10f3343b99a9441bfea8fb23`  
		Last Modified: Thu, 14 May 2026 23:37:16 GMT  
		Size: 5.2 MB (5233725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b84ff3bda7812f7b63b407fe4de3c264fe45b4e761c549bf1ab570937170221`  
		Last Modified: Thu, 14 May 2026 23:37:16 GMT  
		Size: 16.8 KB (16789 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:25f0944fc5188d5a50e748d6a0f796b11927b2641fcd396d9096c262592132a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.0 MB (202970156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583956a49b03b46999795e66e4237f0b6f85c3979df2ab891bf10c6ac7a5ef7d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:43:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:43:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:43:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:43:32 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:43:32 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:55:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:56:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:56:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:56:02 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:56:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac28bbda9cf605f0d239dc381ad9eec484e7e0bec93b2a70b5e743abff1b6d9`  
		Last Modified: Sat, 09 May 2026 02:44:39 GMT  
		Size: 91.9 MB (91914009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4f47fd9138cd0c2159184fa8a0b930eaf53c1911af579346a8d20641b3e9d4`  
		Last Modified: Thu, 14 May 2026 23:56:38 GMT  
		Size: 77.5 MB (77457016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1689f23c5dcd1ddf846e9db90dc24c9f80e9695e26bafb399a3af76ba63e8763`  
		Last Modified: Thu, 14 May 2026 23:56:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b8d1f358dd6c9808f5c0ae2c45b9a8e6f8959dc52e32ed1325eeb6baf834d9`  
		Last Modified: Thu, 14 May 2026 23:56:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eb79d470eace2715118d930a681b53719ea02b08ecfd6987db71e62a9911c8c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea2c3f9aad2a67c230f4be84a84d02b6bd0aadec835dfa5e91d3c21dcd10a02`

```dockerfile
```

-	Layers:
	-	`sha256:eab8991792f8a95664a41d16745809e19efa39af4c704850a7afaa75041e7b8b`  
		Last Modified: Thu, 14 May 2026 23:56:36 GMT  
		Size: 5.2 MB (5215630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d34c84f4203e30630f832d6e528475442cb5988141245be756827445a4a481`  
		Last Modified: Thu, 14 May 2026 23:56:35 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:0e5ebe1d1dbe9f9635d946d6050ea5a0cebf46ba2d0e2bbf097d1ee6a6de9115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191276555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f99df409d0db4a858d57a850dcad3ebbb7ae3d68fa562f72e7342bf59948142`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:38:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:38:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:38:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:38:16 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:38:16 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:38:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:38:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:38:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:38:31 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:38:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6952bb1d663535da0dd5c38e39c53fd423c23c012766a00ed8340a9bae4ab0a1`  
		Last Modified: Thu, 14 May 2026 23:38:59 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef04e6bb2963610cf361e0348ec67e31ab4cdbf0a169f20e636041e20f4a5314`  
		Last Modified: Thu, 14 May 2026 23:38:59 GMT  
		Size: 73.0 MB (73014843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667592f027f933b0e450888d895639a5f2e797d3cd7635235157f0b39b28cb54`  
		Last Modified: Thu, 14 May 2026 23:38:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5403b9f4daaa1353b0fc3a8cc8f0fa13c2d61170fb23e33238fe2a804baebf9`  
		Last Modified: Thu, 14 May 2026 23:38:56 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d28d55805bd72ce807e7dc9eb5a5040241467459af266cf0f2775b6f4c779ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6764c32217d63dc1a6e62840a96eab907e3fc57ed1af47c92eb0faf7313e387`

```dockerfile
```

-	Layers:
	-	`sha256:34c2d19c395d0ab528c22dfd83f30e9d45295eff522c5b3c91bd1ca494ea960f`  
		Last Modified: Thu, 14 May 2026 23:38:56 GMT  
		Size: 5.2 MB (5208421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6274c93af5a9c35d01c0c76d98db48de757d2f2964ff5b73af738d05d8e47d93`  
		Last Modified: Thu, 14 May 2026 23:38:56 GMT  
		Size: 16.6 KB (16647 bytes)  
		MIME: application/vnd.in-toto+json
