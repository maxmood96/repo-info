## `azul-zulu:26-jre-headless-debian`

```console
$ docker pull azul-zulu@sha256:9eb7b94da179e7e4c4d6b1270769afd3be48377a614b435c18fd1f22a6d9984a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:6a6fb1447623f5b7b1c4334a0448762094d81cfefb5eef1da23534c4e881b63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119838249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c806451c57d116da7f4427b588b5743673870bc7122b3d2ed3407f754194d80`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:46:42 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:46:42 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:46:42 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:46:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f8bec0de1ff2132f91c09b31bf16ee2a14531aa2f52a711b951269f046f23a`  
		Last Modified: Tue, 07 Apr 2026 01:46:55 GMT  
		Size: 90.1 MB (90062609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f9c0a4f5f0f64edbced5b7a6918432564e7e2f08758da36888ad2f690817b36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a505e77500f85814c65c33e7812af318fec01b01342301fdc0837f002111188`

```dockerfile
```

-	Layers:
	-	`sha256:8a2839a794387ad513b000c78fef53021924e6c0a8e831718bc4e80bb86c1b53`  
		Last Modified: Tue, 07 Apr 2026 01:46:53 GMT  
		Size: 9.3 KB (9290 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:217e5b8dda98ac2c9551d432814a766022f5e61da34113ba1b2c53458809fb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120132178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4b703e226a9f5f2dc696e74b326486398559d9b740b9838407b6ffc486dd9f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:06:48 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 02:06:48 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:06:48 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 02:06:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9bfc822de02074eca7f99442bd895fb15dfc0d74bfca091c4f8fa055caa421`  
		Last Modified: Tue, 07 Apr 2026 02:07:02 GMT  
		Size: 90.0 MB (89993627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:18874d22aa13117bb456a6c44f4d0a1e4cba1bd9a14800c235213fadbe43fb7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981bedb076655dfe0965694df66289839b9eb7dd7fde87a593bfdc259f0675bf`

```dockerfile
```

-	Layers:
	-	`sha256:09664380ca4f833f4115ab65860d0e760e2199a06a2b1225871600da01355938`  
		Last Modified: Tue, 07 Apr 2026 02:07:00 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.in-toto+json
