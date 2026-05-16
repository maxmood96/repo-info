## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:f8e9459304c24b21dfbfb7fbfa5f595c88a9c33aea704190c0c2daf7b99c83d6
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:06e9990b2c6e16fdd3723b69a036e6b40f1237d206768895cf0cb29ce9aa1f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (259994323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078eb9e0c2c5b76610d3e8a6e6d064aa214048a08b3a1805f1f1ede018e67fd0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:15:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:15:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:15:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:15:32 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:15:32 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:15:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:48 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea298a53c9e20ec0239a76f1509245b920d7aa22ac80d38533509023c452135e`  
		Last Modified: Fri, 15 May 2026 20:16:14 GMT  
		Size: 158.2 MB (158166957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed010eb190dc8492b75117accfd0440dc68c3c8f38288b32b429696aff97ce17`  
		Last Modified: Fri, 15 May 2026 20:16:11 GMT  
		Size: 72.0 MB (72046099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af73ba590d3e38c803d2ed5c1904367ffbb6ef38432797d506363989494bcbf`  
		Last Modified: Fri, 15 May 2026 20:16:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d9de63a8a710e82bad2792291998d053926b93cabf2117ba842a1e7470c2fd`  
		Last Modified: Fri, 15 May 2026 20:16:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0c317c789366186c53c405c814317a333c97ee307952abffc11793437275e5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4da28123ed5552f0aa5fbcae52bf47a8d7e3dbb57550a423b887775a2663e67`

```dockerfile
```

-	Layers:
	-	`sha256:bdab7e8257d96765dd7ff1f8c33b0bc495fe022ac399755e1c343a99127cc446`  
		Last Modified: Fri, 15 May 2026 20:16:08 GMT  
		Size: 5.3 MB (5261705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d5267224d25e2d8e47e9bfab781500be9de0cb26f80ea3adbe63c023eae970e`  
		Last Modified: Fri, 15 May 2026 20:16:08 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:96084cfd9fa65bea56762938a1dbd818268a9c979042adcd84fe49c4caed99bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258460736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b7371876f4b605a5b344dec1c881e769c274a16866494aa63e379669725606`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:15:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:15:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:15:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:15:32 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:15:32 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:15:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c4e9786ff499cd4f94715b4cbbd066253f778bed1b82da38fd2e7b8ed35b0c`  
		Last Modified: Fri, 15 May 2026 20:16:13 GMT  
		Size: 156.5 MB (156461282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e46397d2d6a44384f904b9f2300f6e23e7ce10511f984482ee10ec1822a5c09`  
		Last Modified: Fri, 15 May 2026 20:16:12 GMT  
		Size: 71.9 MB (71854769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173dbdabdddace52ec00c1b77b95a225c2885a7e4ca5a2c332365237dc99fb41`  
		Last Modified: Fri, 15 May 2026 20:16:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2668753e612ff0ca4ffc0eb41f71b7863f568b3683da389c5fea7c395ef4342c`  
		Last Modified: Fri, 15 May 2026 20:16:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:73befc14709389a9ad241d81d17871ef8726628264ff104856865a271946e904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5283557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0f220bbcd3548e400490a4aacdb7b8ee8b4acecef1751720352f6831c6f99c`

```dockerfile
```

-	Layers:
	-	`sha256:167dc1914d53514b5b358b7f389c07daa04e9761d85531170e0fc922fc15afda`  
		Last Modified: Fri, 15 May 2026 20:16:09 GMT  
		Size: 5.3 MB (5267474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e422a34513216cb4f99378b071edb2940c2c8c840fd308f5bbcba90ea2d36fee`  
		Last Modified: Fri, 15 May 2026 20:16:08 GMT  
		Size: 16.1 KB (16083 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e817fac9d32647520c3b52f303bd23dc4abed842090b3bb13fee1a13e92c44e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269398646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56704d898525347cd0ae177dfbb0fa63e395af6ed46109e1c0c51506d94cb561`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:37:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:37:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:37:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:37:56 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:37:56 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:30:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:30:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:30:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:30:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:30:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9429fc219825eaf2a233c26bd84cdc3eef77eb70dd8fad888800a28c7609e2e4`  
		Last Modified: Sat, 09 May 2026 02:39:07 GMT  
		Size: 158.3 MB (158343282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afc6c187204cf5615f44697bf9a615145efb166ef57d2343b22f8b8e11090c0`  
		Last Modified: Fri, 15 May 2026 20:31:29 GMT  
		Size: 77.5 MB (77456237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc7eeb9f004b964bfb5864b58e3f312857bd3bbe52ca4757bfb59f8b0ca7e93`  
		Last Modified: Fri, 15 May 2026 20:31:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dee112fe3ca36efed02bcda7209647b7f910a22e3b3d32ddb6e64ac5f92b16c`  
		Last Modified: Fri, 15 May 2026 20:31:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aeefdcdc2cdcd04e03458bc0c7b461633cea9a2f2c86f24b8a3dc97953c5c9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54218182ea599e96d5b7d495c203451844d1b2ed9ca3b744126a52f591fbfb1e`

```dockerfile
```

-	Layers:
	-	`sha256:e23bbc54757871a4a1e4a2fa8f304820ae59e4ec61c1231c21da5118dfd714fd`  
		Last Modified: Fri, 15 May 2026 20:31:27 GMT  
		Size: 5.3 MB (5266076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b741602841b76c0b4c966002c1e257eacc7dfb99e6b73a7d5e0ee0e1d248a3a4`  
		Last Modified: Fri, 15 May 2026 20:31:27 GMT  
		Size: 15.1 KB (15059 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c13c8f1a0ac6bca079a51ddebc768819ca05c43009b0f422ce8a6de6f2cad6e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250245012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38414178b2264e9ddb35f598618e383e14e39e9e2b51634d7811dd441b593975`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:29:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:29:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:29:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:29:25 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:29:26 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:32:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:32:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:32:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:32:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:32:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d6b2e9210ade672c80e699b87d922bc5ac522046d84e1a1c114ba8bba4ba9b`  
		Last Modified: Fri, 15 May 2026 20:33:58 GMT  
		Size: 147.4 MB (147388338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0f250b19c784ccc4f3a23cc2ebe95ed57132e5946e720eb4d6e15606589e70`  
		Last Modified: Fri, 15 May 2026 20:33:56 GMT  
		Size: 73.0 MB (73015282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0e04e1d54bf0e5b667077684c85ca0088110875248520347cdf096e0a0833a`  
		Last Modified: Fri, 15 May 2026 20:33:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff1a672faeeeb99c835924a363c2b3625d72034fc038af297c3c2a2c565cc18`  
		Last Modified: Fri, 15 May 2026 20:33:51 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:68662129c3962cd1534393f72a871d321e3a59d36c7d584a8a60878a8bc30ed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65b75fb8859b7e10808b52aeef125f84ba8a53e5f97d1b5a34bfcdf08f91b07`

```dockerfile
```

-	Layers:
	-	`sha256:23fab76404bea38cad4191261762e4e6c38574aa47ebc3a9733d924c53affe6c`  
		Last Modified: Fri, 15 May 2026 20:33:51 GMT  
		Size: 5.3 MB (5257629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83688abe2b110d4f53909a08b1ceb757374b175b303924bbaa52f47af2d70e5d`  
		Last Modified: Fri, 15 May 2026 20:33:49 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json
