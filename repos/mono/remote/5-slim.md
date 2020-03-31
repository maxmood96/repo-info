## `mono:5-slim`

```console
$ docker pull mono@sha256:4ea576a28dd48200ea137f74d4191db3f4ad43ad5a1ccaee886f9fb434bb1ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5-slim` - linux; amd64

```console
$ docker pull mono@sha256:f76de3e15ebf2e6b8857bc3ba426abb656fd3237dece954f0e1cc2f8415de2b5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78277061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf91b469701e2d4be79fff2b3ee2f9d2ac9ecf1c8088873c5a76091656ac8965`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 20:55:51 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 31 Mar 2020 20:56:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 31 Mar 2020 20:56:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b5755347d44e006a3743488432c6a77d081bcc3b67cee3609370ca29e83804`  
		Last Modified: Tue, 31 Mar 2020 21:27:55 GMT  
		Size: 244.5 KB (244461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652e7215b25a09c4468906d2f9dd0e353a17465cc5be4ce2a3d2c093ea079f75`  
		Last Modified: Tue, 31 Mar 2020 21:28:08 GMT  
		Size: 55.5 MB (55519226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:7d3d8ed381c901432b3bd1cdfc18c37173ae100c6d421eabd4014c148136051a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45700482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e98c5bd8f807576689c32c4aa2a204dd1c847f5b749b2d6a988db653564f448`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:29:22 GMT
ADD file:dc4797b571cfcef4e94dbdc2465bf637c6d5ac7524c5214e30c580bdeb7af99c in / 
# Tue, 31 Mar 2020 01:29:24 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:19:00 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 31 Mar 2020 04:19:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 31 Mar 2020 04:20:10 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:35e1018f6d3300aef284b3c6ad325d590ecf77d6f3a0163127dc12d599bcc2bf`  
		Last Modified: Tue, 31 Mar 2020 01:36:52 GMT  
		Size: 21.2 MB (21190940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f2c6d2ff90b70ed6371d828f7ee831af4a31004e90c23da734c5f71a096208`  
		Last Modified: Tue, 31 Mar 2020 04:30:57 GMT  
		Size: 244.6 KB (244555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949fd96fbe4244eae7d75bf83abf0e842e1dfa10fffd06486b40000e8280ff6f`  
		Last Modified: Tue, 31 Mar 2020 04:31:06 GMT  
		Size: 24.3 MB (24264987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:3b0b2cde41a8aff48f25933cc369d5f4562ef0740dc851c75da314f483051efa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43105068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f774a689af93577724168d532939c03d5ae54083c2a0230cadacbf1c6a26524`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:52:50 GMT
ADD file:1e233b688c850d7a8a47f185e6f7bb82ad66d729fb1714ecced354cff7be80cd in / 
# Tue, 31 Mar 2020 01:52:52 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:29:59 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 31 Mar 2020 04:30:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 31 Mar 2020 04:31:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4d2af5687ff47f04bedeb1936ed8fe931d68c5684a6959606402065ca5dcb2c5`  
		Last Modified: Tue, 31 Mar 2020 02:00:11 GMT  
		Size: 19.3 MB (19298305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b48266cdd9aec1324b1bf4891a8785c3eaea703b58079cc1560651230efc45f`  
		Last Modified: Tue, 31 Mar 2020 04:41:25 GMT  
		Size: 244.6 KB (244579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf72b0438d7b4d96a1a09f9653a7abd9cfe6a96027473c7b70d6142a94885c64`  
		Last Modified: Tue, 31 Mar 2020 04:41:33 GMT  
		Size: 23.6 MB (23562184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:1179f9b893a6cd70357ced371bafb12aee724f4bf05992c1efe24a46cc0addc1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48771632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b505962662fc0dc529e81036a65c7438f4779143e60cf6da53acf4b91f4078`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:41 GMT
ADD file:002dfad10aab7242b4c5779d19cdca9d7fc4c9fc6fdfa8ed7f282c459fab5da4 in / 
# Tue, 31 Mar 2020 02:08:44 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 05:23:25 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 31 Mar 2020 05:23:45 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 31 Mar 2020 05:24:23 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:43bf72d10816e9fab289a20d17eb586989e2caecbf80328a1c24f031683c350a`  
		Last Modified: Tue, 31 Mar 2020 02:14:33 GMT  
		Size: 20.4 MB (20369961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c72c20695de5948629aa03956878abf6dd63adbd6bf44840f2aed9aeb554c0d`  
		Last Modified: Tue, 31 Mar 2020 05:33:59 GMT  
		Size: 244.4 KB (244379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5786f91fa748586b698deeef02e56fd9993713aef0abc854cfc08350f512b1`  
		Last Modified: Tue, 31 Mar 2020 05:34:09 GMT  
		Size: 28.2 MB (28157292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; 386

```console
$ docker pull mono@sha256:5d3e7048238f2c2d379e8c926710fc1a0a41978fa5d443df809ebf3f635579c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81943143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583976489b8730ecf5a701072aa47aaf3a3323c64c2961ffccb4a3fce079592d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 00:42:50 GMT
ADD file:3b9d63dd21a9a32c414c2ec2fda6cd46b6d0ea83cd89b56de0f238f27458082f in / 
# Tue, 31 Mar 2020 00:42:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:39:22 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 31 Mar 2020 01:39:31 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 31 Mar 2020 01:40:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7101806a3a87632f9e8e3ed7e99547db8d61727cb461d50f91fa2099ee987d87`  
		Last Modified: Tue, 31 Mar 2020 00:48:47 GMT  
		Size: 23.1 MB (23141421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53e3ca1225543eb8bfa1be6db4cc7e2c202294f029d26dbd978601866b307ee`  
		Last Modified: Tue, 31 Mar 2020 01:47:40 GMT  
		Size: 244.5 KB (244474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2add50b12e8dfde1df681e658e771cc0bbecb6ba6c3b01f4cc621362521a0cff`  
		Last Modified: Tue, 31 Mar 2020 01:47:56 GMT  
		Size: 58.6 MB (58557248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:371b05ee8225078652681f5106d4142fb6fc23f64ed9639ee8493b074ba51a9f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47669583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664aa8aea66a18f502ab838cf7fbcf54c2912f8606dea41c8c2e540f325981db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:36:47 GMT
ADD file:18fbbcdf5b1b1e93b849dccfac9d28a25ed63c4c13f3e6cb141579d7474401e7 in / 
# Tue, 31 Mar 2020 01:36:53 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:34:13 GMT
ENV MONO_VERSION=5.20.1.34
# Tue, 31 Mar 2020 02:35:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 31 Mar 2020 02:37:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:12443815c8d74f5cceb21d06ea95ceca887ebe0a6f2e2084bd2131a6ad9c6af0`  
		Last Modified: Tue, 31 Mar 2020 01:54:08 GMT  
		Size: 22.8 MB (22785257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c3f8dfc8f601e918a4678c6bf8884395eb229531eee30c248a05f25ce2110d`  
		Last Modified: Tue, 31 Mar 2020 02:58:51 GMT  
		Size: 244.7 KB (244682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d51afab87d01405681bcee723260d070c2974cac0794271af710ae5ae5e61bb`  
		Last Modified: Tue, 31 Mar 2020 02:58:56 GMT  
		Size: 24.6 MB (24639644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
