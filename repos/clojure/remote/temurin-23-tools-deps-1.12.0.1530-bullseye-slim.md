## `clojure:temurin-23-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:1b622a22cba0e3937c2636ec327b0e7d894c466cc5aeb9433044197cd35e737e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:657f0897bc320c8d98c495a28119fa36acfad0e56d6ac87cb3bff86e2c48ca5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254355914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d72a1fb338d110bd515390e95ba26c534d7064a86728ce5741b6647eb45721`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069596e310dfe895da22fe6575b69b2ccfd2b388d3ae220fd6fd90de51854dec`  
		Last Modified: Mon, 10 Mar 2025 17:40:23 GMT  
		Size: 165.3 MB (165316201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d6577884e79f8d8e94cafefa411ae6004a8551804bed154255a6fa0b79a769`  
		Last Modified: Mon, 10 Mar 2025 17:40:21 GMT  
		Size: 58.8 MB (58784741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de6efaf9cf0c30cca8b7c199c1c1e3adc13f51551cc064a851efb6dc9566e34`  
		Last Modified: Mon, 10 Mar 2025 17:40:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2ab911216148010e0ba1b614efeedd3d5df1d90d7fe4c7beceb574441b72a6`  
		Last Modified: Mon, 10 Mar 2025 17:40:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d60e346a28d5a1d1a4115e56dff748ff3927acc2bba21b9a63c109c1d0ed0f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597d13d99d125b5732a068fdfbc8d8ae9657ec1faabbab01518ff3005b5db6fe`

```dockerfile
```

-	Layers:
	-	`sha256:9ee73d0e278104c56d40532c7e88f29eff4d95b9ed89471647d0f1f557388cf7`  
		Last Modified: Mon, 10 Mar 2025 17:40:20 GMT  
		Size: 5.1 MB (5122072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee90edee8e32ceb11c58022178b242ce9a9ff804670f0c69ed826871db901168`  
		Last Modified: Mon, 10 Mar 2025 17:40:19 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d69e39afdf3e6c8230f03b20236357fe6d80d109ece6921f2f82e2a8b33cc172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (250997039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10769758e16bb1b8b4b4b7f9377cbb6ac1949b96a4df00b85d77da98bacc999c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67df4c94cd7aa41d87bb022ebe304300818b97b628b4256b53dcb16a1340d0b9`  
		Last Modified: Mon, 10 Mar 2025 17:56:20 GMT  
		Size: 163.3 MB (163341441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bfb8ec800eb7368391518fa2a18c2ebdaa5f9f44afecb6eda9ab6a87550de6`  
		Last Modified: Mon, 10 Mar 2025 17:56:18 GMT  
		Size: 58.9 MB (58908568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736558a854e31f53bb8ee6f03c8db6dc3dd9ac1a3daed51cbf558676d80db234`  
		Last Modified: Mon, 10 Mar 2025 17:56:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1786306cd7612c80e10433d2829ea208cd54cbe58f6fa8465efc5bafe865b098`  
		Last Modified: Mon, 10 Mar 2025 17:56:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:262c2aebd449dfcee128615d7ca4f980abbce093695704cf15d320e04fb2626a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b769d4a6c518c1aa0eda755066554468a572fd6d81f1be709e591c461eaa1f62`

```dockerfile
```

-	Layers:
	-	`sha256:a6a6584a1e1c0eda57f1b925abdc1d8a72f5801708c8a56946dbbd4b74542b38`  
		Last Modified: Mon, 10 Mar 2025 17:56:17 GMT  
		Size: 5.1 MB (5127183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98e14c5211552709ef614588b9bf5c893fb905e4288d6b1f19a1581baee6f628`  
		Last Modified: Mon, 10 Mar 2025 17:56:16 GMT  
		Size: 16.0 KB (15993 bytes)  
		MIME: application/vnd.in-toto+json
