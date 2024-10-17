## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:c2d83e8f13dcd02573a347db7df5a126ff1fe7851e9edb1f674de32cf0daa2d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1d3c2af8585d75f41c84236c035a0c1ad89d5867bcc4396ca4974704af5e9d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248949274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a4e234d6b4fe5b04652fe0509cb1b237d6dc86514b1beb01885e228074b0bc`
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
	-	`sha256:f7286d488f1fccdf17634c3ed2f4e10a4d10c8c1ffc8cedeff6033be2465e7b5`  
		Last Modified: Thu, 17 Oct 2024 01:13:40 GMT  
		Size: 158.6 MB (158579255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e17f61d3180448d81dfa943f399cd35e408f08e1b70a7cc0c73f59c22f6092`  
		Last Modified: Thu, 17 Oct 2024 01:13:39 GMT  
		Size: 58.9 MB (58940182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff94bd3688e421e36baebfbad65bf7d96dfe5c4a58b0fd1476bbddbd93d30f8c`  
		Last Modified: Thu, 17 Oct 2024 01:13:38 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d21bc1709ae0169c40fa1c2e97c34ab538107d16e594aac8a66d1a454fafe`  
		Last Modified: Thu, 17 Oct 2024 01:13:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4667eb4bacd1da456ead04a5badd12677afbcc2e45d13c27c493df9ffc1deafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5119619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d89abed3366f0df95a16211f549ecc24341c1b61c175d4f21ee1fb2d67325b`

```dockerfile
```

-	Layers:
	-	`sha256:544a998cd392be340a0d67a2ea79384c0193ebff340bb3a17fa89a9f2da3dbde`  
		Last Modified: Thu, 17 Oct 2024 01:13:38 GMT  
		Size: 5.1 MB (5103372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b1e9b3d48f2e0e834f9348533a0637e7743e7982316448b517451c5b783824`  
		Last Modified: Thu, 17 Oct 2024 01:13:38 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

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

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f1a08e705c1f63e02bd45bed468302bf3d3beb27c5687e7b49e4fd2d7708ad23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bddba01c365d58638783a4bdac5f9def041970e551f5b2bfc1b3a13bb9b92ca`

```dockerfile
```

-	Layers:
	-	`sha256:d67e703b1538fc7721efca251b8add14ccb36456d6cb5b30a1fcc422b4311812`  
		Last Modified: Thu, 17 Oct 2024 08:26:32 GMT  
		Size: 5.1 MB (5109133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5289685e300f4bb4af88b6da8cc0610259d242e1313c34c1a0fdc27ab4f82d1c`  
		Last Modified: Thu, 17 Oct 2024 08:26:31 GMT  
		Size: 16.4 KB (16375 bytes)  
		MIME: application/vnd.in-toto+json
