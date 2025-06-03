## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:fca77bdf6507b5e94eab02b47b848d72fd7e8e1c6d27f4e0440440d6a8d473a9
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dcf75a5907d6cbb04ecc24ae4d134d5a292f718b1042b35e2b0543ea29f0e87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255391774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8636cd00df112c0c716336261a1a94323fabd118e572a236c2fe623501f615`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c213a88d50e16dae04348c30f8ce7f7db5972cacaf24dbe06c0912bf4f0874d5`  
		Last Modified: Tue, 03 Jun 2025 05:16:47 GMT  
		Size: 157.6 MB (157634492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c57ca51a5c0fb43a55088d07f824f62f7bd2789a949b69af54cf5fafd33795`  
		Last Modified: Tue, 03 Jun 2025 05:16:46 GMT  
		Size: 69.5 MB (69530912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967ed07d5448b0bd36b019e59b6453835ac640eb6f9d112e3e76e11e55a54edf`  
		Last Modified: Tue, 03 Jun 2025 05:16:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481e0bd5f3b1dc3381a4b4402c5eb3f6063fc5d06a3fcfec88c2b6f026803a7d`  
		Last Modified: Tue, 03 Jun 2025 05:16:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0cd1a176545e1ac7da749c222ecadad435124994de36dcf1bce57c0b2d8ddca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4981871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7e130721ecd4b48b20b4ec52f4ddbcace20532cdc0bd3f96785f731fe67069`

```dockerfile
```

-	Layers:
	-	`sha256:b6f4405b20c48797af28e92f567493be355e14aeed1ec928cbbba39e85f9fffe`  
		Last Modified: Tue, 03 Jun 2025 05:16:44 GMT  
		Size: 5.0 MB (4965296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0369eaff4733a69ba4b2ef4a31b019f67b4a115fc98856965d1bbaa2bb6ab723`  
		Last Modified: Tue, 03 Jun 2025 05:16:43 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:472b3e992b251bc740b05576ed924ba8edf58f56dc6771b88945d8a48bebfc5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253381231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92300a2cd98036729e9a37bed5aece528a32d674c112c38e5df0193b71268429`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b920f2782e54c0936283f35994e494b7bf3269bc82c414f10cec27aba0c88c7c`  
		Last Modified: Thu, 22 May 2025 08:29:52 GMT  
		Size: 155.9 MB (155928808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2210aa8eba8f23b1aa674fa25a493b53439b03040502635f13fa431a7285ecd`  
		Last Modified: Thu, 22 May 2025 08:34:58 GMT  
		Size: 69.4 MB (69386103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88593c1f56760164d0bdffced0a919b9c51fc03ef31749dc1b6add14896a6f1`  
		Last Modified: Thu, 22 May 2025 08:34:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1847f5f11a81fd19c14e7acc7700802e8aed0ec770890eda2fa0f55d20ed3c`  
		Last Modified: Thu, 22 May 2025 08:34:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e6547270c39fe566b746bc6d76103a3a59dd83d2914d7c261b5141725c3bb36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4987798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6bf3aad480487abcb20c7d0c84d0d4745321c7962f5f180db71ffd5cebbf71`

```dockerfile
```

-	Layers:
	-	`sha256:4a89cad8d47c1d0bb93cf7c00c780042c71c16da31c2affb9da9f32c4986fa5e`  
		Last Modified: Thu, 22 May 2025 08:34:56 GMT  
		Size: 5.0 MB (4971081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8129d0f5e94352a063e88b8dc6da9df48d16e3e0d681f21d03d5ca49d725d6`  
		Last Modified: Thu, 22 May 2025 08:34:55 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ff3d8f9bd9559ef5aff41f420443a38f761d0db2868f58736e3582db97cdd7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265220379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8d354d7da3c7c9bc424a787f338d83c5c8dac24fb2c8eabb095fbeae9c29d0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4096b52192e932752b9bcceca4f9d004fc84df91d2241bac974844eab93d96f9`  
		Last Modified: Thu, 22 May 2025 11:29:02 GMT  
		Size: 157.8 MB (157804907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d094e53115a2c4a4d7bc935505879ddc7ab2b0a196e4ade0ca31a2b797671da`  
		Last Modified: Thu, 22 May 2025 11:36:36 GMT  
		Size: 75.3 MB (75347517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc80f6fbb7c18d5f2feb72f4f090bf909c410e156dac2d33763235ba20851a`  
		Last Modified: Thu, 22 May 2025 11:36:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a51bd848b6c69bb1615bd6eae8410e7f34f23731ce862a9d26e72e605b65603`  
		Last Modified: Thu, 22 May 2025 11:36:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c65f5604cd6a8a268252223a61628ff09f8cb3f867125066a88c73dd6f60c5aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4987101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d6294482074be0fd34cc59f897542930f2e8c6913933408e445af9416cb803`

```dockerfile
```

-	Layers:
	-	`sha256:cd52e5eade3c145c0958f181c761cd0f2fc92cfff92050387635b5fc9a4f1068`  
		Last Modified: Thu, 22 May 2025 11:36:34 GMT  
		Size: 5.0 MB (4970466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab1d28768bdc7e618cc3c2d7744c860b838478149f5b41fca9ba3f1af807588f`  
		Last Modified: Thu, 22 May 2025 11:36:33 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:78d7dc432208323998af7becf4aa0c692e6472a7a690e48e204fe1a883e11579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242121863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a98a88e89e8db2ff3f829541ca3a0f6b3d70a1acf1519f2f33cf571299a21f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833ce0de8cf4c008922a20ce0f4a2e515d9892f114fbc6b544b0dc1f28845f2b`  
		Last Modified: Tue, 03 Jun 2025 06:25:04 GMT  
		Size: 146.9 MB (146910974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af55f60ff2637ed87ea844f99f9ab01a50c803c4223ed4b292479a2035f35be8`  
		Last Modified: Tue, 03 Jun 2025 06:30:53 GMT  
		Size: 68.3 MB (68327045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebb306f4d3af4814ecf4f2ca0b73406122222096d2e1d4a601fac80fb2e9a23`  
		Last Modified: Tue, 03 Jun 2025 06:30:51 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837b631e6fb843556cd1ebed7a02580283a8a8318b9246dc28491918a8614b94`  
		Last Modified: Tue, 03 Jun 2025 06:30:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:903e8a959c49113cd9f9d3a915dda53d1dcc14e6d5ae75f9c4c6d97a7a39a744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4976084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc837d77004aad5a8f3106fc24fa84e8bfd37dc7033ca905c73ea06c50f4dca`

```dockerfile
```

-	Layers:
	-	`sha256:5942a0d0d6b67e151958f4deb88999d4fff5691a42c75543718566d2700eafeb`  
		Last Modified: Tue, 03 Jun 2025 06:30:51 GMT  
		Size: 5.0 MB (4959509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9970396f048e861f5042d5656a74c438590af5b4e493afcb9b858d2f252e2a9f`  
		Last Modified: Tue, 03 Jun 2025 06:30:51 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json
