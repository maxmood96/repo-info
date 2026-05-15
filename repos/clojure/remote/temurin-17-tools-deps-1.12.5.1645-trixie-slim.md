## `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim`

```console
$ docker pull clojure@sha256:013341bac183d2585559bca61624b3b6d2df679baf9528e2aea9663e240197d4
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

### `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a68f8553cb7ccd25c0f41d9326fa3a3ec06bca25782bdcf4673223bb9a429be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247732715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010bc05fb0b88c6bb262124cd42ef42158fba5d130b33186c2e073d4a388ed50`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:14:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:46 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:46 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:15:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9dac3eb7b18631052e0f3a6d583f20a8f2195d910d57325c9c2dc737155cff`  
		Last Modified: Fri, 15 May 2026 20:15:26 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddc541b6b87bbc2f2efd1c728164a6592f39ba562336f6674fe2eae8ecbc07d`  
		Last Modified: Fri, 15 May 2026 20:15:24 GMT  
		Size: 72.0 MB (72045989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760b27cdf0fdcb31d04c1b7e05072ffc7cf271ee24e1954f84f775a7836a44df`  
		Last Modified: Fri, 15 May 2026 20:15:21 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677135c9e45be5a2789e5138b1a6b3a7a56485aa70bc9a9a59e5bed5474bb51a`  
		Last Modified: Fri, 15 May 2026 20:15:21 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d0eb1dac8994752a0a984894fb6ec545fdd4fd433bb3f8140192db30a9237cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff3e27ea3e681d797451055b00983df55b21c3e6ad60e78a965d36e9799901b`

```dockerfile
```

-	Layers:
	-	`sha256:82b0bb0aa483f191857f73f416928549153e73428e5eaf2989b7640c6cd57dd1`  
		Last Modified: Fri, 15 May 2026 20:15:21 GMT  
		Size: 5.3 MB (5259853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8df2b597a88b6c4d4482bee0f7d2e7e90b24a59c14acfadb7fc037bc9abcfa95`  
		Last Modified: Fri, 15 May 2026 20:15:21 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ec773fc3c61f640bcddb9108e0bf16f56a7540ad2f62415ef340389c1ccf08a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246723818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ec435ca1c7d3a666069cf932a3866aa37514f4abe86557bb6b2d0eb46e885b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:15:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:15:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:15:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:15:06 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:15:06 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:15:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7f0fcbd3f4d437a3df3c5b5b5196058702a3f96b65c28b7e0b6bf4ab4ac2e3`  
		Last Modified: Fri, 15 May 2026 20:15:52 GMT  
		Size: 144.7 MB (144724358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb73958a3fea67481283202410ca1d3fdc406424da933a2ec488aeec81b6f81`  
		Last Modified: Fri, 15 May 2026 20:15:44 GMT  
		Size: 71.9 MB (71854778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4af8b27e01762529a766195d09d5f2e5a79f2d7e31d2b80ff3dc0585213a9f`  
		Last Modified: Fri, 15 May 2026 20:15:41 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e717d0ac7278bbeab3b83ee57e7c3f4f4472b55ba583b3eaa8fe18bface6743c`  
		Last Modified: Fri, 15 May 2026 20:15:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b1f4882a6fe93f2fad2808f7fac04951cdf79d12e7f6058b213be88817f78c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673ea9b4351e33c42f0614795a8b99baf4b2bc87d821610abdd612fdfbe88e06`

```dockerfile
```

-	Layers:
	-	`sha256:5b18be637f1c602fdc4058628c917472617eabe83303277cb6258aa7084783da`  
		Last Modified: Fri, 15 May 2026 20:15:42 GMT  
		Size: 5.3 MB (5265622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb0a357b52197fddad1a8855b0d80071c07170c74a63b24cf2c95d5f300af3d`  
		Last Modified: Fri, 15 May 2026 20:15:41 GMT  
		Size: 16.1 KB (16084 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f3b02f957c37fbc1fa242dd736835cb20520ff22be847b848f297dbf36409a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256821439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8d46824ec2fe914a9a0809d4c66db4b66d0ebaa2ab004be8b4fb57542bb387`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:32:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:32:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:32:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:32:03 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:32:03 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:26:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:26:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:26:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:26:31 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:26:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f72cabc9601635085bc11fa48d74114d9e1765a07685bad636cd3a7da9370ac`  
		Last Modified: Sat, 09 May 2026 02:33:09 GMT  
		Size: 145.8 MB (145766215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a6e1403bb0602ad9dd6c3cd7be974b170038472916b67f7728e6a212bb19cd`  
		Last Modified: Fri, 15 May 2026 20:27:07 GMT  
		Size: 77.5 MB (77456095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976fa490c8c4e2ffd8b959c58c086e64132d722f43d74a86eecd0cb66f45ad5d`  
		Last Modified: Fri, 15 May 2026 20:27:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5460bc3a0f4833eebbcc937e1377815a22b3c099b545c61b96ea1a2b68318ce`  
		Last Modified: Fri, 15 May 2026 20:27:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ce9311fe925d367f6e4dea3e04031cc96411432599d1de97229a93e55779eb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dd7ddab9ab84a62be92a8e2b709f9633670430b7d656467b2acff0a0601925`

```dockerfile
```

-	Layers:
	-	`sha256:4bc491786ea639ee44ee9978e9a4b93d5f7c81c6189dee72e0723ba05b9121bb`  
		Last Modified: Fri, 15 May 2026 20:27:04 GMT  
		Size: 5.3 MB (5264224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fa24eaad8a5c8ce03e69dbff106bf08e4df55fe0a0c1da34ca5a0f9391236fb`  
		Last Modified: Fri, 15 May 2026 20:27:04 GMT  
		Size: 15.1 KB (15059 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b1aeca3f39701dde213fad7e08701bb4b11afa1fe928ef2cb6d2b853aff3473e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.8 MB (238767522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0bc39017035bb491a40af35b27ad4b815434abc44d391da667e2749f718c704`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:35:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:32 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Thu, 14 May 2026 23:35:32 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:26:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:26:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:26:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:26:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:26:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeabeb56e1eebe9b1edc136c9b084b501f34255e33a2b2c7f5f66dcb37c977db`  
		Last Modified: Thu, 14 May 2026 23:36:20 GMT  
		Size: 135.9 MB (135910407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54542e054e95f3a328878dcd5cba018694dc4e323712549ce58762ef87e1fe5c`  
		Last Modified: Fri, 15 May 2026 20:28:04 GMT  
		Size: 73.0 MB (73015724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91eaf3c339079d392fdbe4d6ceee0d9b511cd477491ecfb893b654c501f9e277`  
		Last Modified: Fri, 15 May 2026 20:27:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50d8d03ed0f7295d58e7567b92b0a052665b39d97b9e693d01dd214eaee360a`  
		Last Modified: Fri, 15 May 2026 20:27:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f529d1a519eaa3f64aeceddf581b3ba3f5f4fbcdbe51cb234997f782db4e8468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065bc67e6754187f807e8e53a793caac972641054450cfa9b09fc13d4472ae6f`

```dockerfile
```

-	Layers:
	-	`sha256:698ee9ed3f7f74bb3b440fc9bdb344a92b53dff4195c79b270395af84b60c48d`  
		Last Modified: Fri, 15 May 2026 20:28:01 GMT  
		Size: 5.3 MB (5255777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e70454192b6a3fa8c8ff3db67936a9687f17126f3f56603a600ff723672fbbd8`  
		Last Modified: Fri, 15 May 2026 20:27:59 GMT  
		Size: 15.0 KB (15011 bytes)  
		MIME: application/vnd.in-toto+json
