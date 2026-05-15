## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:8520afb5749d19ec786f5495c68cbf33f999e2b68b961a6725838c1a122a5af9
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

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f2b2a4dec0976caf1f6b8ccb38bf09651b5aa74a5673aaf67d3234c0f30068cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275608914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843a875dc0e23fcac5e4947732de078964b1eb074d93ece3dbd662e0e9283da9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:14:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:31 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:31 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:14:44 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:14:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba33b1d4cb730692434069f311792283c7fac67df9b421f2fecb96cc14665755`  
		Last Modified: Fri, 15 May 2026 20:15:08 GMT  
		Size: 145.9 MB (145905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151ddd2d32ce93224a197f6408f0e60c03106fe334b09ea08e60bc6535d888eb`  
		Last Modified: Fri, 15 May 2026 20:15:07 GMT  
		Size: 81.2 MB (81213714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d10f62d7dc9998b556994819e756ca7f33183e1b46e434754c469a7009557e`  
		Last Modified: Fri, 15 May 2026 20:15:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971fb889b32d79bb9eb1068447d812f38f5b70f5fb75b464d45e6adc3b5f72e6`  
		Last Modified: Fri, 15 May 2026 20:15:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5f8f9571f42629f57ab8ec4747b7979fafb7ee9f6408151db8e5725e82bd6172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc4aaacf536465b2db93cc41ec126cc940c2316daee62b1d7705395b87df23a`

```dockerfile
```

-	Layers:
	-	`sha256:7b2df6d03fd01eb3c5b2e2aff6804091da9dd2c56e48f9993cc732a40b68c7c1`  
		Last Modified: Fri, 15 May 2026 20:15:04 GMT  
		Size: 7.4 MB (7378927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f59c0744bf927f04903c1ab894d16a7cf987cb9b77c4d8ed6c9b6d01091451c1`  
		Last Modified: Fri, 15 May 2026 20:15:04 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d5c8e94779c7c1266837c637365ba941c1d3f21a2558f1a31ce02c510e797fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274293018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:848a3ed723e00a50d8e10f5e639f69986935d0a49ec19624215d575da4ea4c86`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:14:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:29 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:29 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:14:44 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:14:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0165d03f4d8ef42f486a8c958ef476295dc421ff3ba3f154304386b6841dcd7c`  
		Last Modified: Fri, 15 May 2026 20:15:08 GMT  
		Size: 144.7 MB (144724336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53596aff5e4c8613e8426c60f5c171961aa35b4758aa65cf3f33b499d8cb937`  
		Last Modified: Fri, 15 May 2026 20:15:06 GMT  
		Size: 81.2 MB (81194489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc33f43bc7498ddbedeac2fa7d9ce762d81db7f83c7aba56e491333e27accc7`  
		Last Modified: Fri, 15 May 2026 20:15:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848e5292bf3cdb98a48e52b08157da9dfedb448b85cc6d21543d2e65bbdfaae3`  
		Last Modified: Fri, 15 May 2026 20:15:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:62137b9d1584eed2213ec0d014e5368517ec64c2663e4880f8b29b2cbd9309dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9cf4680acb57497ccd690c1dc59b6f8c8bba466aaa1ce5f5c1d94107a4b1c3`

```dockerfile
```

-	Layers:
	-	`sha256:5c3746ee6837fd8ce9e1b3a571217fbbbc04b8ac1ececa1ac440b92461c9a6a8`  
		Last Modified: Fri, 15 May 2026 20:15:03 GMT  
		Size: 7.4 MB (7384690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3367d040840e6ceb342c1c06def5c2346cb58f4e08343095365ad53ddf992251`  
		Last Modified: Fri, 15 May 2026 20:15:03 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:5438e44222ed91139752fc436b94d6ab23dddcacdd746dcb6e01529801847da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285137415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98ba6d18c4763c5e6b875571cc51435d0be60160246b0674c5ea238e3d105a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:30:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:30:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:30:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:30:22 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:30:22 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:22:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:22:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:22:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:22:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:22:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8690ec3700a5aee074ea4c1951ffc72590a2a8686be7918dee225def8496211d`  
		Last Modified: Sat, 09 May 2026 02:31:26 GMT  
		Size: 145.8 MB (145766181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c877d29d3913e36cb82fd9714c0f387fed91db5ba198aece9ade037ee4bc082e`  
		Last Modified: Fri, 15 May 2026 20:23:23 GMT  
		Size: 87.0 MB (87033402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b918edcc20a6fc473cb4120ca8f2282498b7f05be9db7ce53dcb1c70d1976e55`  
		Last Modified: Fri, 15 May 2026 20:23:21 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba179b609f64c1653db0ccdcfda097a7947107d98fec81e7815115a6293bb0dc`  
		Last Modified: Fri, 15 May 2026 20:23:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ea386f411ee74bd17437da474fff4a297b5123ede6d56c0dac9cc7d0a2685560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7911a32d1457a2c19a04f4aeab8ff26484f1f890724ea13ad2806334a55011eb`

```dockerfile
```

-	Layers:
	-	`sha256:71dfa2c59ff2f92c98a820c0e2cdc6be0ffe8dbe0c3be6dbc74a929c88cf510b`  
		Last Modified: Fri, 15 May 2026 20:23:21 GMT  
		Size: 7.4 MB (7384143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86176127ada39651f1152e337df09933dfbf8f8be7f8928140334905cd56fe5b`  
		Last Modified: Fri, 15 May 2026 20:23:21 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:f320de4a04223767b477ed35a7fa7aed2d6f927423bf13d33a74a5ab7b114ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263085451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e34fa5cb65f8008ee4b1ba56a2aee99c602efcfaa2692163faaf0777af6512d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:14:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:48 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:49 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:17:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:17:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:17:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:17:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:17:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9057b51c5535b33fc79fb5796b4f91080e9f4c6d669e9de704fbb30e660aaf`  
		Last Modified: Fri, 15 May 2026 20:18:41 GMT  
		Size: 135.9 MB (135910447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab4398b482eef4dc7bd4344a11f9af10434097ee08f29366f1b8d09df608f6`  
		Last Modified: Fri, 15 May 2026 20:18:38 GMT  
		Size: 80.0 MB (80025937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805213598bf771a69872c2ec0be9f715fc90cde2a91b0c8416d324a9ff874767`  
		Last Modified: Fri, 15 May 2026 20:18:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e22c705e7fa3a51d844da35290987756aaedec4af1ac8f467f26737bc42daed`  
		Last Modified: Fri, 15 May 2026 20:18:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7821292435551a996d9834ec427b2dde89b446613d0951a216a8e220176f46c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6817f9b6b0f40eb0b7fd774e3751c7ece2e414a3834bff4bec87acca0ee6a625`

```dockerfile
```

-	Layers:
	-	`sha256:7ffaddbda4a6b932836ec458d00c31488d66a62214d5c3e899de7a54f34328b9`  
		Last Modified: Fri, 15 May 2026 20:18:31 GMT  
		Size: 7.4 MB (7370246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:284446cedfbd8bbe8df546411729e1d1c9b6a6fa83bfa20b2a451d9a19f6ac06`  
		Last Modified: Fri, 15 May 2026 20:18:31 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
