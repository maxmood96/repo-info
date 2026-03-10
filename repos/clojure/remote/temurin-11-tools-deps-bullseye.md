## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:95bd90e110bfd463fea87c7939a3726a359d59c4f14fa8721f9a79822ab12611
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:722abfda477f25cda2fa6131e2a8863e24f409fb46c88820b19a45f5c109e6e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269151567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ffac1005ec76f83eec7b7cb2315af20e7cf52352bbf0bf0b538960821659c5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:34:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:22 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:23 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a602d819236cad2809342b1ddf49c3f8fce808d306dce9c7460eff94c656f75`  
		Last Modified: Mon, 09 Mar 2026 20:34:58 GMT  
		Size: 145.8 MB (145806749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f1a814d012f298515969fc032324ff2c251e0701eb0902b42977200d99d4a9`  
		Last Modified: Mon, 09 Mar 2026 20:34:56 GMT  
		Size: 69.6 MB (69587738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e706664af415adb36b585ab8c424269dcccb78f89b923be50bf54c57b0f090`  
		Last Modified: Mon, 09 Mar 2026 20:34:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d4dccae2bc703a298dc701321e7751211f1388cf33949a31599d8443bab14f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7443627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316bb7c7baaf74a693baf1db5d22ab1a6ef219de47694b226512684c0fb965bc`

```dockerfile
```

-	Layers:
	-	`sha256:a9c10f27a0b05943393bc02687285a177d1357ca22340197402ffb6909100c58`  
		Last Modified: Mon, 09 Mar 2026 20:34:54 GMT  
		Size: 7.4 MB (7429418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2b8a9ce16b4163db4e0868867c0e33eebb89beebf5de3916c824121f863ffc4`  
		Last Modified: Mon, 09 Mar 2026 20:34:53 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a0b403575df89d4cc9b96c39214bf2ece820d5a3ddcb733dacfde98d4e5aec53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264489165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5990df6c7ad4dccc25e82ae0d50984d92b08d1b0fe503d094d7b4cf8b5a8cd`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:34:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:19 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:19 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687d5e7aec5ec88ed5013221039cedc831f5e4fcf7c2dd77bc9657f9bb40b3dc`  
		Last Modified: Mon, 09 Mar 2026 20:34:58 GMT  
		Size: 142.5 MB (142501446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41a14f490c90934cbaa17dece8aff1c979793ac50e9a69b4b1b1e557bcf5225`  
		Last Modified: Mon, 09 Mar 2026 20:35:05 GMT  
		Size: 69.7 MB (69728680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de448bd87410ce64009f99616467a2ca5e5cad1d846fbdbd17b28e4e5ffe1831`  
		Last Modified: Mon, 09 Mar 2026 20:34:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0f78d633f02e6e8e2e60a022af68d262353116ae1d550ff16c14964bb87c3b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7449462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56f0bac0ecf5af9d81c8f14551f4210962de9c14d1b81ef21f0d2908b49b515`

```dockerfile
```

-	Layers:
	-	`sha256:abf12f974d706e61e3e6246a7ebd1115ed0745c58e15cb687c5d54cd1aabf0eb`  
		Last Modified: Mon, 09 Mar 2026 20:34:51 GMT  
		Size: 7.4 MB (7435135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90a8708e42ca7c4143641510ec5867c17ad9ade0bfd4d06cb3c856536f0e7aee`  
		Last Modified: Mon, 09 Mar 2026 20:34:51 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
