## `clojure:temurin-22-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:74d32cd882fff055b8995f5a07774d9aeb19ac8b1e804e96b75c87133b94246f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:375247121e3ccc321b52c29bae163e9643374f9259fc549b814ef25768896c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280822158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a61e579d3bb7890189badd42d4321d810c7bd03d11a24ba29b596a6545b1ee7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905958096e83919efcafc488e2f97abb45d45d5e688c610940fc5e43388524c3`  
		Last Modified: Tue, 23 Jul 2024 07:14:21 GMT  
		Size: 156.7 MB (156715516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8e957cbfe1507d451999d958ddb1149525cfebe36cd124993fdd1a2dca1370`  
		Last Modified: Tue, 23 Jul 2024 07:14:20 GMT  
		Size: 69.0 MB (69021022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b930f828aca4ed14663f5f5ab07ca03d36ee01f529bddd1f038fd95eccbc3db0`  
		Last Modified: Tue, 23 Jul 2024 07:14:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41bcd491f4ecc5c8389db4016b30f9ceadec8766c4885c477642474d50188abc`  
		Last Modified: Tue, 23 Jul 2024 07:14:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ed919530f54b1f2e19144a7922463ef58fc0befbe1694b790e1f767bca34749a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7055777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bd16766d190122c5cf43f0fc661be2df3f90d6289df539516130ea8637aa12`

```dockerfile
```

-	Layers:
	-	`sha256:a44661aecebdcb4e1f425c74c13f08dc2d46ed7a59457f7ce5acb21294cc3454`  
		Last Modified: Tue, 23 Jul 2024 07:14:17 GMT  
		Size: 7.0 MB (7040338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fb1155c576d01a8ec6796ebf6236a20780184aacea549f9a2bacf72921d4c67`  
		Last Modified: Tue, 23 Jul 2024 07:14:16 GMT  
		Size: 15.4 KB (15439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b95efd067ba39c64f2552b0006bec89633644e20c15f99729169ba3867f2619c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277593907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93db248d8cc91a0087934165b5054eeb3287f5b7c2287dc76fde0e51127b7adb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a82e743f56fdd5686b4686e09264632831459e3e7ed605c7fff5bf27a78249`  
		Last Modified: Tue, 02 Jul 2024 09:45:19 GMT  
		Size: 154.7 MB (154738019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca738c59d7b1b7b0e62d5bc1f74fe66e8a83ab97772d9778ee904110a3b4f989`  
		Last Modified: Tue, 02 Jul 2024 09:49:17 GMT  
		Size: 69.1 MB (69133194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed021fc34d95381d029d83851f4a19e165d24d77648ea47c1ae5ec9bb1b11d2a`  
		Last Modified: Tue, 02 Jul 2024 09:49:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b1768addbd6401596d13e36b9d5c2f07147bea3c0c740ed5946126f16abe34`  
		Last Modified: Tue, 02 Jul 2024 09:49:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:88db20f54a5e3830fd0c76b3d9c43f3f9f38e954a748a24c9574f1301fcc9733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f65ef151c4e9a1ff64eefd50a8d202fc0612e1f906cfdc0f8ddd67db1e89061`

```dockerfile
```

-	Layers:
	-	`sha256:63c8dec7693948209677298085381f2686fa84153db4db881e6e18c90572a1e0`  
		Last Modified: Tue, 02 Jul 2024 09:49:15 GMT  
		Size: 7.0 MB (7005506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48540aa05a0448b47750121d05f5811c33943aa2dbf68cf7b925276da583cc0a`  
		Last Modified: Tue, 02 Jul 2024 09:49:14 GMT  
		Size: 16.0 KB (15974 bytes)  
		MIME: application/vnd.in-toto+json
