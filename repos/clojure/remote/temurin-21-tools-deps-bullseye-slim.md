## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:6fcbaa7ee2019937c9910f7c55f5a7a6594f640e0d1bc00184640638b0894f16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:61cd98f64be66a77fce15dce98f16a3b39ec735d89ddf80aa45e2e42dc9fe2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248949111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f8dff6eb0fd9833c7166b03763b7f0d03d854eea2a22ab0df00b72a9faa8cd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28164b117ee5ccf2499c2719e4510a0661fadf730c634c5e85e771078b783ba3`  
		Last Modified: Sat, 19 Oct 2024 02:59:46 GMT  
		Size: 158.6 MB (158579286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0eddb8a459981c88518f4e42ee6f985a6ef18c8ab27b628101d94d0e239f35`  
		Last Modified: Sat, 19 Oct 2024 02:59:45 GMT  
		Size: 58.9 MB (58939984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eec2d9c03d040f300aa3884658ef5fa35a6205f95e4e3bb2a5da2b228b29fe`  
		Last Modified: Sat, 19 Oct 2024 02:59:44 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fb1e85ab6ef45edce047374dfb280ddcdef86659ad09b737c7583c3de535be`  
		Last Modified: Sat, 19 Oct 2024 02:59:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:89cb31544ff7ac3a811f237fa9ecba2484b99bc499007b1c7ca09fcba5599bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5145532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbe5ff5e563c0510579fac74b27c49594caaff23343957d88e27ba384ae6563`

```dockerfile
```

-	Layers:
	-	`sha256:375f36838dbf8f98b0bfd653e10067f6c3ab9fc19b7ff8022154849ffc438e57`  
		Last Modified: Sat, 19 Oct 2024 02:59:44 GMT  
		Size: 5.1 MB (5129117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1452678ac583ce478a57b9fcb3bc94db723394cad870cf03fa61634d9606eed`  
		Last Modified: Sat, 19 Oct 2024 02:59:44 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ee5e6d2e8cb18bc5856e51cabdfa1fb6dfab388b7a46cee1f2bfaf025d54ebfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245896155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3d52586fe7493e5cbe6ab4302c8dbd8eda121441581185842c276f63593cdd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3fc741297801fb172b0488da69efb29652404502b115a1b69118ef76478eef`  
		Last Modified: Thu, 17 Oct 2024 08:22:07 GMT  
		Size: 156.7 MB (156746189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e005c22c4ad05475fa470a75cfd59720033ed388ef8720322c02a65b9fedcce5`  
		Last Modified: Thu, 17 Oct 2024 08:26:34 GMT  
		Size: 59.1 MB (59073169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09366a90beffb97051638b023775e32d68dd10d82b5f5c35db11a969445a69a`  
		Last Modified: Thu, 17 Oct 2024 08:26:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953d82401425c1e7037bfe4d51c35b0ee38a47d5b6a11c1b2202424ce51198de`  
		Last Modified: Thu, 17 Oct 2024 08:26:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:08ca8b9025e8957b3d99cf4d4069b309b5ae2a2850f408da66ff09d0ae3e780c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626591e868d4ccf544f45ff91830c3e4e03216f32dcb3cb0e1d9f0f6d2d7e2ca`

```dockerfile
```

-	Layers:
	-	`sha256:a048f4b479cd90ec5fc4e540f4f6c146101071b253c8a6fd84b510b8c7118b4b`  
		Last Modified: Sat, 19 Oct 2024 12:16:56 GMT  
		Size: 5.1 MB (5134878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9c67810eafcb1c03a5922e7e4ec91dd260305efb9cd5819b51b2a53fe71ed5`  
		Last Modified: Sat, 19 Oct 2024 12:16:55 GMT  
		Size: 16.6 KB (16551 bytes)  
		MIME: application/vnd.in-toto+json
