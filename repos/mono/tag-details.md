<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mono`

-	[`mono:6`](#mono6)
-	[`mono:6.10`](#mono610)
-	[`mono:6.10.0`](#mono6100)
-	[`mono:6.10.0.104`](#mono6100104)
-	[`mono:6.10.0.104-slim`](#mono6100104-slim)
-	[`mono:6.10.0-slim`](#mono6100-slim)
-	[`mono:6.10-slim`](#mono610-slim)
-	[`mono:6.12`](#mono612)
-	[`mono:6.12.0`](#mono6120)
-	[`mono:6.12.0.107`](#mono6120107)
-	[`mono:6.12.0.107-slim`](#mono6120107-slim)
-	[`mono:6.12.0-slim`](#mono6120-slim)
-	[`mono:6.12-slim`](#mono612-slim)
-	[`mono:6-slim`](#mono6-slim)
-	[`mono:latest`](#monolatest)
-	[`mono:slim`](#monoslim)

## `mono:6`

```console
$ docker pull mono@sha256:188caea1633590c0af93df6462db94366998d465f4f654b3c6759b9ebf875dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6` - linux; amd64

```console
$ docker pull mono@sha256:e3c3faa1e0eccfec442341c7260bfb1faeccf40581fe8a00e77e794cf27d150b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235856726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d02da61afa912e62ef7cdc2e3b89fb6915716c72eccd75293b5c784ba17e5ce`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 09:40:56 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 09:41:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 09:41:33 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 09:48:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe02677df6f8831edfcea8a4558dcbb344dda0a234033ce403a445f71bb95e04`  
		Last Modified: Tue, 12 Jan 2021 09:56:50 GMT  
		Size: 255.9 KB (255924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6f0c1d36d945478bb94f4061ab9e9570a42d064b1bac55d482cc3d9eefdc1b`  
		Last Modified: Tue, 12 Jan 2021 09:57:04 GMT  
		Size: 67.1 MB (67079218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55acb8a81f9716f19bc8b425a4f2f9778868a086ced2c38a0d232c7e149e260b`  
		Last Modified: Tue, 12 Jan 2021 09:58:10 GMT  
		Size: 141.4 MB (141413515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:1d24028dba828fdc96b2b742b714f446f92b64abd6d180f3941954836178a989
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191752100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bcdc117695b526e00f4bac23d6c63d036306f5db62472b44bb3778d586032a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b88dcc371a0eb826a2922cd9da711f02c951f809c2d794f69ed376a2fece59`  
		Last Modified: Tue, 09 Feb 2021 04:20:55 GMT  
		Size: 140.1 MB (140107311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:c73416458bcb7bf5fa69488bd6815e282f46605e12f39a780d06ca20f5bc052d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187637328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808ec81fbec92ca5875883f0c5df523025c9784692513d2affb1e388dc139163`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195bce90b1707cb6f414c434f6348a2daa6c8bce4b713a9a1fa52e0d024305de`  
		Last Modified: Tue, 09 Feb 2021 04:20:29 GMT  
		Size: 138.9 MB (138939518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:bb8bcb03c776a1d69c8402a77aeb49e7302fca102ab82e11002ca319287ae33a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214424611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8b3b0d88c8a2f9826ad928f5035cd23a14395c38e57da6f376205bb25ac8d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 05:07:35 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 05:07:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 05:08:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 05:12:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c624bef28ff9228422eef122ec713693eb2e8d2ed78aa41f319bd0678a607c`  
		Last Modified: Tue, 12 Jan 2021 05:15:20 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ec950da6523b4cb54939edc61c6460d64327528adc05f607fbf005ff508a88`  
		Last Modified: Tue, 12 Jan 2021 05:15:34 GMT  
		Size: 31.7 MB (31720550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0470c4fa675956b4e41164ba69e70c7c53cbf56fa1fde6ca99247fd30d63182`  
		Last Modified: Tue, 12 Jan 2021 05:16:54 GMT  
		Size: 156.6 MB (156583646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:3f6d7e510f3c7e210af3336de41288b7e8971519c559d7994389b5aaab7ca0d6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241641989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7d8ae0005ba40c7547dfff94755167dba0e74f722bd8583e10d292d8cc13d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:36 GMT
ADD file:601e9b729a871ae893eafa56eeac5d5d2c93a1bd60786560aae25b3644295a23 in / 
# Tue, 12 Jan 2021 00:39:36 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:55:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:55:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:56:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 03:59:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a5116b3c01b9daadc6c4605561821b0e7f908a2d339a79315de7651174cd76d7`  
		Last Modified: Tue, 12 Jan 2021 00:46:26 GMT  
		Size: 27.8 MB (27767991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ae7e24292b47c5c54d019f27f833b4d1fd06c6c1760426a915f4626d13ebb5`  
		Last Modified: Tue, 12 Jan 2021 04:01:42 GMT  
		Size: 255.9 KB (255867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f6fae6c251aafe4f2903014f5ca67d695cd2f74f87cc46b0b9b5e50650a9f`  
		Last Modified: Tue, 12 Jan 2021 04:02:03 GMT  
		Size: 71.1 MB (71105792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a6a59d3738ce8d2e6bad95e51859928eac584152411a872b1dfd4ec6cbffe4`  
		Last Modified: Tue, 12 Jan 2021 04:03:29 GMT  
		Size: 142.5 MB (142512339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; ppc64le

```console
$ docker pull mono@sha256:8cd03e8a315754c3631020ef221a2d0cbd0992577901c899c47ce5e69d61dd49
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203325644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be23bd3cc106fdd913dd4eff53c1f46dabb535e753abef0f566dae2c69eaea9d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:34:09 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:35:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:37:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 03:52:04 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e77824b16d99ee079aa03b8aabec031637265f7380c082326eaf48d078a93e7`  
		Last Modified: Tue, 12 Jan 2021 04:01:02 GMT  
		Size: 256.1 KB (256146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8e3bf2452dcba3a8621830f987ddbcc051bd5b6d5817e6d595c1cd93497f67`  
		Last Modified: Tue, 12 Jan 2021 04:01:08 GMT  
		Size: 29.3 MB (29311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be798b1b9507d975e13d056b87d688839b0f83115176be62486731bf9cac3ed7`  
		Last Modified: Tue, 12 Jan 2021 04:02:25 GMT  
		Size: 143.2 MB (143225573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10`

```console
$ docker pull mono@sha256:42bbe689251fbe538577d9cfe14053ed8e40615c17c120486044c5428aaa46c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10` - linux; amd64

```console
$ docker pull mono@sha256:4310626243c7cb039164506a632955ff6f88b33d9cd7ca81821248f14134bd92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224747979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c04af7238369a5f5f0c473aad5bff633bea9a4d1b45ac888947f38d34d19bd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 09:41:43 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 09:41:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 09:42:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 09:56:24 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e54505e49395a0d6a43f271952bf307a05153f6510a80ae27038c50df0efa46`  
		Last Modified: Tue, 12 Jan 2021 09:57:16 GMT  
		Size: 255.9 KB (255924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187e7566eb41f21ec1afcdd35f44280fdc2057d58a74789bd9affda7da2084a4`  
		Last Modified: Tue, 12 Jan 2021 09:57:29 GMT  
		Size: 67.1 MB (67092827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045d12fef3a002ecc26a8a290b60da3b7e004e0102ad78ea21be87c04ea4b331`  
		Last Modified: Tue, 12 Jan 2021 09:58:59 GMT  
		Size: 130.3 MB (130291159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v5

```console
$ docker pull mono@sha256:5af63248159aed358b06ada57e95e308ea1c223a298088d91422fd0ce00f40e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180632533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8478ed95add121817e320c0f83fe2b60aa2b2dbb1cf8229d680f2d56dbd5ce38`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:23 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:18:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cb1c784014fc8011ca8f4610f5131311b17486b9d6077606eaddacde5a2c27`  
		Last Modified: Tue, 09 Feb 2021 04:19:46 GMT  
		Size: 256.0 KB (256004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4b453be37d3b9ff06672c4a993a5489066cd5c2df5d33b2e6a60b32cadecdb`  
		Last Modified: Tue, 09 Feb 2021 04:19:58 GMT  
		Size: 26.6 MB (26575039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b135eeb77d4910d732e79e8132148b43949a28bc3d231923f3de862124ab98`  
		Last Modified: Tue, 09 Feb 2021 04:21:55 GMT  
		Size: 129.0 MB (128962193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v7

```console
$ docker pull mono@sha256:8d39d372380f5a73de1f4c13baefe5fe30208504c2ee87a5c3a46da5d2c5a7ef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176550748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c3606599470c3663a458214939b09b22fac76dba598915323586f15dfa2c41`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:18:18 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7698330b69a6c19085fab2ed78c48495acb00c18a4ffc6e0f6f40d54b9421b50`  
		Last Modified: Tue, 09 Feb 2021 04:19:18 GMT  
		Size: 256.0 KB (255991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44741965a508902c904fb46c6cdf26919ecb482fe42acc022eede0e3bab5e501`  
		Last Modified: Tue, 09 Feb 2021 04:19:28 GMT  
		Size: 25.8 MB (25775825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c95880f81ec1d835fef70912336e6b01cad3de5a478b93b5e46c148f4247812`  
		Last Modified: Tue, 09 Feb 2021 04:21:35 GMT  
		Size: 127.8 MB (127815548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:cb1208b1b962d03ac3d2de8aa234bd08e1f8586a273ace18118ea9915b28a088
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203319469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da43b28377f75813f7cfcf7e574e53c7a3e8ed73f7cf24058c27d860e10db29e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 05:08:43 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 05:08:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 05:09:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 05:14:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6179e732b6b6a778fbe4321833a5ba71f60a206504e6a1a93efe345ec9aedf3e`  
		Last Modified: Tue, 12 Jan 2021 05:15:48 GMT  
		Size: 255.9 KB (255937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79964378e1ae7824bc19481d96933ec96cd27ade28c334215d53bafbab3e5d53`  
		Last Modified: Tue, 12 Jan 2021 05:15:59 GMT  
		Size: 31.7 MB (31749798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6950b481095c08dd42a719f4427100df6a0eb94de69f3c82e5aa3f666570601d`  
		Last Modified: Tue, 12 Jan 2021 05:17:57 GMT  
		Size: 145.4 MB (145449242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; 386

```console
$ docker pull mono@sha256:53975b45852e0214be6a8f7a4451adad23a40b2457fd5c40e7239ad2dfa47dc8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230551724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3e85181b4a6d18083325fd95e4472863ede71e1b0857650c9621564e9a3e98`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:36 GMT
ADD file:601e9b729a871ae893eafa56eeac5d5d2c93a1bd60786560aae25b3644295a23 in / 
# Tue, 12 Jan 2021 00:39:36 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:56:09 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 03:56:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:56:56 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 04:01:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a5116b3c01b9daadc6c4605561821b0e7f908a2d339a79315de7651174cd76d7`  
		Last Modified: Tue, 12 Jan 2021 00:46:26 GMT  
		Size: 27.8 MB (27767991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae604efc877a26d5e9ef47c0ce73f76fc847780ddc3fc4f4fa2dae62aebc1b79`  
		Last Modified: Tue, 12 Jan 2021 04:02:20 GMT  
		Size: 255.8 KB (255850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5562f2f87a9508fba6e611a28b8bc7747b5368845e5cfa71f1a25a457f2c1e`  
		Last Modified: Tue, 12 Jan 2021 04:02:42 GMT  
		Size: 71.1 MB (71136255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10581e73388ee9a7aa52a53d415eaa9b6ecc1a57fb2426de84e028895c80d7aa`  
		Last Modified: Tue, 12 Jan 2021 04:04:16 GMT  
		Size: 131.4 MB (131391628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; ppc64le

```console
$ docker pull mono@sha256:582dd336e9dfac08b00f63738182f127e766f6e207a3914f47c35a44ca9c1f20
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192117601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae166434ad1e239a83259bd86e49e76bc0f5aa0071cef7683034da040d80b53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:37:52 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 03:39:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:41:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 04:00:12 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a6b5cd501f71da14d37bddd625494e7a2de28217c260bc74553a9b4bc12b0f`  
		Last Modified: Tue, 12 Jan 2021 04:01:26 GMT  
		Size: 256.3 KB (256256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e85b5bce279ec9104f3a75e8c3a74fbd322ee4fff6244ab3046f12df7348d2a`  
		Last Modified: Tue, 12 Jan 2021 04:01:38 GMT  
		Size: 29.4 MB (29350170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ab9db45435abc9c30283f6ff37a0801fe81b852dca5ecad333bd338711bf55`  
		Last Modified: Tue, 12 Jan 2021 04:03:22 GMT  
		Size: 132.0 MB (131978338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0`

```console
$ docker pull mono@sha256:42bbe689251fbe538577d9cfe14053ed8e40615c17c120486044c5428aaa46c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0` - linux; amd64

```console
$ docker pull mono@sha256:4310626243c7cb039164506a632955ff6f88b33d9cd7ca81821248f14134bd92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224747979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c04af7238369a5f5f0c473aad5bff633bea9a4d1b45ac888947f38d34d19bd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 09:41:43 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 09:41:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 09:42:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 09:56:24 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e54505e49395a0d6a43f271952bf307a05153f6510a80ae27038c50df0efa46`  
		Last Modified: Tue, 12 Jan 2021 09:57:16 GMT  
		Size: 255.9 KB (255924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187e7566eb41f21ec1afcdd35f44280fdc2057d58a74789bd9affda7da2084a4`  
		Last Modified: Tue, 12 Jan 2021 09:57:29 GMT  
		Size: 67.1 MB (67092827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045d12fef3a002ecc26a8a290b60da3b7e004e0102ad78ea21be87c04ea4b331`  
		Last Modified: Tue, 12 Jan 2021 09:58:59 GMT  
		Size: 130.3 MB (130291159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:5af63248159aed358b06ada57e95e308ea1c223a298088d91422fd0ce00f40e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180632533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8478ed95add121817e320c0f83fe2b60aa2b2dbb1cf8229d680f2d56dbd5ce38`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:23 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:18:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cb1c784014fc8011ca8f4610f5131311b17486b9d6077606eaddacde5a2c27`  
		Last Modified: Tue, 09 Feb 2021 04:19:46 GMT  
		Size: 256.0 KB (256004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4b453be37d3b9ff06672c4a993a5489066cd5c2df5d33b2e6a60b32cadecdb`  
		Last Modified: Tue, 09 Feb 2021 04:19:58 GMT  
		Size: 26.6 MB (26575039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b135eeb77d4910d732e79e8132148b43949a28bc3d231923f3de862124ab98`  
		Last Modified: Tue, 09 Feb 2021 04:21:55 GMT  
		Size: 129.0 MB (128962193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:8d39d372380f5a73de1f4c13baefe5fe30208504c2ee87a5c3a46da5d2c5a7ef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176550748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c3606599470c3663a458214939b09b22fac76dba598915323586f15dfa2c41`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:18:18 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7698330b69a6c19085fab2ed78c48495acb00c18a4ffc6e0f6f40d54b9421b50`  
		Last Modified: Tue, 09 Feb 2021 04:19:18 GMT  
		Size: 256.0 KB (255991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44741965a508902c904fb46c6cdf26919ecb482fe42acc022eede0e3bab5e501`  
		Last Modified: Tue, 09 Feb 2021 04:19:28 GMT  
		Size: 25.8 MB (25775825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c95880f81ec1d835fef70912336e6b01cad3de5a478b93b5e46c148f4247812`  
		Last Modified: Tue, 09 Feb 2021 04:21:35 GMT  
		Size: 127.8 MB (127815548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:cb1208b1b962d03ac3d2de8aa234bd08e1f8586a273ace18118ea9915b28a088
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203319469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da43b28377f75813f7cfcf7e574e53c7a3e8ed73f7cf24058c27d860e10db29e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 05:08:43 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 05:08:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 05:09:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 05:14:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6179e732b6b6a778fbe4321833a5ba71f60a206504e6a1a93efe345ec9aedf3e`  
		Last Modified: Tue, 12 Jan 2021 05:15:48 GMT  
		Size: 255.9 KB (255937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79964378e1ae7824bc19481d96933ec96cd27ade28c334215d53bafbab3e5d53`  
		Last Modified: Tue, 12 Jan 2021 05:15:59 GMT  
		Size: 31.7 MB (31749798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6950b481095c08dd42a719f4427100df6a0eb94de69f3c82e5aa3f666570601d`  
		Last Modified: Tue, 12 Jan 2021 05:17:57 GMT  
		Size: 145.4 MB (145449242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; 386

```console
$ docker pull mono@sha256:53975b45852e0214be6a8f7a4451adad23a40b2457fd5c40e7239ad2dfa47dc8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230551724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3e85181b4a6d18083325fd95e4472863ede71e1b0857650c9621564e9a3e98`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:36 GMT
ADD file:601e9b729a871ae893eafa56eeac5d5d2c93a1bd60786560aae25b3644295a23 in / 
# Tue, 12 Jan 2021 00:39:36 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:56:09 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 03:56:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:56:56 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 04:01:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a5116b3c01b9daadc6c4605561821b0e7f908a2d339a79315de7651174cd76d7`  
		Last Modified: Tue, 12 Jan 2021 00:46:26 GMT  
		Size: 27.8 MB (27767991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae604efc877a26d5e9ef47c0ce73f76fc847780ddc3fc4f4fa2dae62aebc1b79`  
		Last Modified: Tue, 12 Jan 2021 04:02:20 GMT  
		Size: 255.8 KB (255850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5562f2f87a9508fba6e611a28b8bc7747b5368845e5cfa71f1a25a457f2c1e`  
		Last Modified: Tue, 12 Jan 2021 04:02:42 GMT  
		Size: 71.1 MB (71136255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10581e73388ee9a7aa52a53d415eaa9b6ecc1a57fb2426de84e028895c80d7aa`  
		Last Modified: Tue, 12 Jan 2021 04:04:16 GMT  
		Size: 131.4 MB (131391628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; ppc64le

```console
$ docker pull mono@sha256:582dd336e9dfac08b00f63738182f127e766f6e207a3914f47c35a44ca9c1f20
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192117601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae166434ad1e239a83259bd86e49e76bc0f5aa0071cef7683034da040d80b53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:37:52 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 03:39:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:41:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 04:00:12 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a6b5cd501f71da14d37bddd625494e7a2de28217c260bc74553a9b4bc12b0f`  
		Last Modified: Tue, 12 Jan 2021 04:01:26 GMT  
		Size: 256.3 KB (256256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e85b5bce279ec9104f3a75e8c3a74fbd322ee4fff6244ab3046f12df7348d2a`  
		Last Modified: Tue, 12 Jan 2021 04:01:38 GMT  
		Size: 29.4 MB (29350170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ab9db45435abc9c30283f6ff37a0801fe81b852dca5ecad333bd338711bf55`  
		Last Modified: Tue, 12 Jan 2021 04:03:22 GMT  
		Size: 132.0 MB (131978338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104`

```console
$ docker pull mono@sha256:42bbe689251fbe538577d9cfe14053ed8e40615c17c120486044c5428aaa46c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0.104` - linux; amd64

```console
$ docker pull mono@sha256:4310626243c7cb039164506a632955ff6f88b33d9cd7ca81821248f14134bd92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224747979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c04af7238369a5f5f0c473aad5bff633bea9a4d1b45ac888947f38d34d19bd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 09:41:43 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 09:41:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 09:42:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 09:56:24 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e54505e49395a0d6a43f271952bf307a05153f6510a80ae27038c50df0efa46`  
		Last Modified: Tue, 12 Jan 2021 09:57:16 GMT  
		Size: 255.9 KB (255924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187e7566eb41f21ec1afcdd35f44280fdc2057d58a74789bd9affda7da2084a4`  
		Last Modified: Tue, 12 Jan 2021 09:57:29 GMT  
		Size: 67.1 MB (67092827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045d12fef3a002ecc26a8a290b60da3b7e004e0102ad78ea21be87c04ea4b331`  
		Last Modified: Tue, 12 Jan 2021 09:58:59 GMT  
		Size: 130.3 MB (130291159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v5

```console
$ docker pull mono@sha256:5af63248159aed358b06ada57e95e308ea1c223a298088d91422fd0ce00f40e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180632533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8478ed95add121817e320c0f83fe2b60aa2b2dbb1cf8229d680f2d56dbd5ce38`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:23 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:18:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cb1c784014fc8011ca8f4610f5131311b17486b9d6077606eaddacde5a2c27`  
		Last Modified: Tue, 09 Feb 2021 04:19:46 GMT  
		Size: 256.0 KB (256004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4b453be37d3b9ff06672c4a993a5489066cd5c2df5d33b2e6a60b32cadecdb`  
		Last Modified: Tue, 09 Feb 2021 04:19:58 GMT  
		Size: 26.6 MB (26575039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b135eeb77d4910d732e79e8132148b43949a28bc3d231923f3de862124ab98`  
		Last Modified: Tue, 09 Feb 2021 04:21:55 GMT  
		Size: 129.0 MB (128962193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v7

```console
$ docker pull mono@sha256:8d39d372380f5a73de1f4c13baefe5fe30208504c2ee87a5c3a46da5d2c5a7ef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176550748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c3606599470c3663a458214939b09b22fac76dba598915323586f15dfa2c41`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:18:18 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7698330b69a6c19085fab2ed78c48495acb00c18a4ffc6e0f6f40d54b9421b50`  
		Last Modified: Tue, 09 Feb 2021 04:19:18 GMT  
		Size: 256.0 KB (255991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44741965a508902c904fb46c6cdf26919ecb482fe42acc022eede0e3bab5e501`  
		Last Modified: Tue, 09 Feb 2021 04:19:28 GMT  
		Size: 25.8 MB (25775825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c95880f81ec1d835fef70912336e6b01cad3de5a478b93b5e46c148f4247812`  
		Last Modified: Tue, 09 Feb 2021 04:21:35 GMT  
		Size: 127.8 MB (127815548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:cb1208b1b962d03ac3d2de8aa234bd08e1f8586a273ace18118ea9915b28a088
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203319469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da43b28377f75813f7cfcf7e574e53c7a3e8ed73f7cf24058c27d860e10db29e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 05:08:43 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 05:08:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 05:09:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 05:14:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6179e732b6b6a778fbe4321833a5ba71f60a206504e6a1a93efe345ec9aedf3e`  
		Last Modified: Tue, 12 Jan 2021 05:15:48 GMT  
		Size: 255.9 KB (255937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79964378e1ae7824bc19481d96933ec96cd27ade28c334215d53bafbab3e5d53`  
		Last Modified: Tue, 12 Jan 2021 05:15:59 GMT  
		Size: 31.7 MB (31749798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6950b481095c08dd42a719f4427100df6a0eb94de69f3c82e5aa3f666570601d`  
		Last Modified: Tue, 12 Jan 2021 05:17:57 GMT  
		Size: 145.4 MB (145449242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; 386

```console
$ docker pull mono@sha256:53975b45852e0214be6a8f7a4451adad23a40b2457fd5c40e7239ad2dfa47dc8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230551724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3e85181b4a6d18083325fd95e4472863ede71e1b0857650c9621564e9a3e98`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:36 GMT
ADD file:601e9b729a871ae893eafa56eeac5d5d2c93a1bd60786560aae25b3644295a23 in / 
# Tue, 12 Jan 2021 00:39:36 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:56:09 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 03:56:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:56:56 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 04:01:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a5116b3c01b9daadc6c4605561821b0e7f908a2d339a79315de7651174cd76d7`  
		Last Modified: Tue, 12 Jan 2021 00:46:26 GMT  
		Size: 27.8 MB (27767991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae604efc877a26d5e9ef47c0ce73f76fc847780ddc3fc4f4fa2dae62aebc1b79`  
		Last Modified: Tue, 12 Jan 2021 04:02:20 GMT  
		Size: 255.8 KB (255850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5562f2f87a9508fba6e611a28b8bc7747b5368845e5cfa71f1a25a457f2c1e`  
		Last Modified: Tue, 12 Jan 2021 04:02:42 GMT  
		Size: 71.1 MB (71136255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10581e73388ee9a7aa52a53d415eaa9b6ecc1a57fb2426de84e028895c80d7aa`  
		Last Modified: Tue, 12 Jan 2021 04:04:16 GMT  
		Size: 131.4 MB (131391628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; ppc64le

```console
$ docker pull mono@sha256:582dd336e9dfac08b00f63738182f127e766f6e207a3914f47c35a44ca9c1f20
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192117601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae166434ad1e239a83259bd86e49e76bc0f5aa0071cef7683034da040d80b53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:37:52 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 03:39:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:41:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 04:00:12 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a6b5cd501f71da14d37bddd625494e7a2de28217c260bc74553a9b4bc12b0f`  
		Last Modified: Tue, 12 Jan 2021 04:01:26 GMT  
		Size: 256.3 KB (256256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e85b5bce279ec9104f3a75e8c3a74fbd322ee4fff6244ab3046f12df7348d2a`  
		Last Modified: Tue, 12 Jan 2021 04:01:38 GMT  
		Size: 29.4 MB (29350170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ab9db45435abc9c30283f6ff37a0801fe81b852dca5ecad333bd338711bf55`  
		Last Modified: Tue, 12 Jan 2021 04:03:22 GMT  
		Size: 132.0 MB (131978338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104-slim`

```console
$ docker pull mono@sha256:e4a01967f524e646e2b249fab2be90f1c4939aa9acc0e33b7ebb914dea51284f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0.104-slim` - linux; amd64

```console
$ docker pull mono@sha256:c844ff3b7ee54eaba943c75712d14160804ef3ab8dabdc1e1c3272e74608a541
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94456820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1c7db5380987c54d84126cba76a6a6dccfaf004120eea20a3d79214279ab2d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 09:41:43 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 09:41:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 09:42:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e54505e49395a0d6a43f271952bf307a05153f6510a80ae27038c50df0efa46`  
		Last Modified: Tue, 12 Jan 2021 09:57:16 GMT  
		Size: 255.9 KB (255924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187e7566eb41f21ec1afcdd35f44280fdc2057d58a74789bd9affda7da2084a4`  
		Last Modified: Tue, 12 Jan 2021 09:57:29 GMT  
		Size: 67.1 MB (67092827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:c712f335d3056624b71f739eab72063f54dfdc9b1e79505f492350d575120386
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51670340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebaa3f292c5fd2c5f88f4c02fde89257131eddc5ecc1b5f4ab3aefb23f54cf7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:23 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cb1c784014fc8011ca8f4610f5131311b17486b9d6077606eaddacde5a2c27`  
		Last Modified: Tue, 09 Feb 2021 04:19:46 GMT  
		Size: 256.0 KB (256004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4b453be37d3b9ff06672c4a993a5489066cd5c2df5d33b2e6a60b32cadecdb`  
		Last Modified: Tue, 09 Feb 2021 04:19:58 GMT  
		Size: 26.6 MB (26575039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:1f06a597ee6d31d6be24bc45bd61b8bdbf82f41e4d20c6693c0562118c8c44d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48735200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9c6e0275747a42fb6d529c5e573d92cb73aed4ef196a5dd6421239f57cc5d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7698330b69a6c19085fab2ed78c48495acb00c18a4ffc6e0f6f40d54b9421b50`  
		Last Modified: Tue, 09 Feb 2021 04:19:18 GMT  
		Size: 256.0 KB (255991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44741965a508902c904fb46c6cdf26919ecb482fe42acc022eede0e3bab5e501`  
		Last Modified: Tue, 09 Feb 2021 04:19:28 GMT  
		Size: 25.8 MB (25775825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:6948940e8f06496863e933abbc4535ffbf2a6809be7a8ad57ba0472a7e425757
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57870227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48136d057bf03e9368936fd11090def9dea2ab83438eeb50225f1c3b77208e98`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 05:08:43 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 05:08:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 05:09:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6179e732b6b6a778fbe4321833a5ba71f60a206504e6a1a93efe345ec9aedf3e`  
		Last Modified: Tue, 12 Jan 2021 05:15:48 GMT  
		Size: 255.9 KB (255937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79964378e1ae7824bc19481d96933ec96cd27ade28c334215d53bafbab3e5d53`  
		Last Modified: Tue, 12 Jan 2021 05:15:59 GMT  
		Size: 31.7 MB (31749798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; 386

```console
$ docker pull mono@sha256:23a7d61d14921fb6cdac9af3089bbe43d4802f95e94f5783e68d8665d14f9ed8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99160096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1183437f303f6695f81fc122467d5294b0b29e6038bafbce0e5afb2e84dc8ac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:36 GMT
ADD file:601e9b729a871ae893eafa56eeac5d5d2c93a1bd60786560aae25b3644295a23 in / 
# Tue, 12 Jan 2021 00:39:36 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:56:09 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 03:56:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:56:56 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a5116b3c01b9daadc6c4605561821b0e7f908a2d339a79315de7651174cd76d7`  
		Last Modified: Tue, 12 Jan 2021 00:46:26 GMT  
		Size: 27.8 MB (27767991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae604efc877a26d5e9ef47c0ce73f76fc847780ddc3fc4f4fa2dae62aebc1b79`  
		Last Modified: Tue, 12 Jan 2021 04:02:20 GMT  
		Size: 255.8 KB (255850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5562f2f87a9508fba6e611a28b8bc7747b5368845e5cfa71f1a25a457f2c1e`  
		Last Modified: Tue, 12 Jan 2021 04:02:42 GMT  
		Size: 71.1 MB (71136255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:dcf3bae1c6fc5c089a7c08cc5d902422dbe8047387242a2f451937b6bc571788
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60139263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9427fdc99870b74f065955ba37c7bac20a528e45dd0092c6cd6f305c7181ea22`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:37:52 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 03:39:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:41:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a6b5cd501f71da14d37bddd625494e7a2de28217c260bc74553a9b4bc12b0f`  
		Last Modified: Tue, 12 Jan 2021 04:01:26 GMT  
		Size: 256.3 KB (256256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e85b5bce279ec9104f3a75e8c3a74fbd322ee4fff6244ab3046f12df7348d2a`  
		Last Modified: Tue, 12 Jan 2021 04:01:38 GMT  
		Size: 29.4 MB (29350170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0-slim`

```console
$ docker pull mono@sha256:e4a01967f524e646e2b249fab2be90f1c4939aa9acc0e33b7ebb914dea51284f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:c844ff3b7ee54eaba943c75712d14160804ef3ab8dabdc1e1c3272e74608a541
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94456820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1c7db5380987c54d84126cba76a6a6dccfaf004120eea20a3d79214279ab2d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 09:41:43 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 09:41:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 09:42:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e54505e49395a0d6a43f271952bf307a05153f6510a80ae27038c50df0efa46`  
		Last Modified: Tue, 12 Jan 2021 09:57:16 GMT  
		Size: 255.9 KB (255924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187e7566eb41f21ec1afcdd35f44280fdc2057d58a74789bd9affda7da2084a4`  
		Last Modified: Tue, 12 Jan 2021 09:57:29 GMT  
		Size: 67.1 MB (67092827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:c712f335d3056624b71f739eab72063f54dfdc9b1e79505f492350d575120386
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51670340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebaa3f292c5fd2c5f88f4c02fde89257131eddc5ecc1b5f4ab3aefb23f54cf7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:23 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cb1c784014fc8011ca8f4610f5131311b17486b9d6077606eaddacde5a2c27`  
		Last Modified: Tue, 09 Feb 2021 04:19:46 GMT  
		Size: 256.0 KB (256004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4b453be37d3b9ff06672c4a993a5489066cd5c2df5d33b2e6a60b32cadecdb`  
		Last Modified: Tue, 09 Feb 2021 04:19:58 GMT  
		Size: 26.6 MB (26575039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:1f06a597ee6d31d6be24bc45bd61b8bdbf82f41e4d20c6693c0562118c8c44d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48735200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9c6e0275747a42fb6d529c5e573d92cb73aed4ef196a5dd6421239f57cc5d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7698330b69a6c19085fab2ed78c48495acb00c18a4ffc6e0f6f40d54b9421b50`  
		Last Modified: Tue, 09 Feb 2021 04:19:18 GMT  
		Size: 256.0 KB (255991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44741965a508902c904fb46c6cdf26919ecb482fe42acc022eede0e3bab5e501`  
		Last Modified: Tue, 09 Feb 2021 04:19:28 GMT  
		Size: 25.8 MB (25775825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:6948940e8f06496863e933abbc4535ffbf2a6809be7a8ad57ba0472a7e425757
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57870227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48136d057bf03e9368936fd11090def9dea2ab83438eeb50225f1c3b77208e98`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 05:08:43 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 05:08:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 05:09:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6179e732b6b6a778fbe4321833a5ba71f60a206504e6a1a93efe345ec9aedf3e`  
		Last Modified: Tue, 12 Jan 2021 05:15:48 GMT  
		Size: 255.9 KB (255937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79964378e1ae7824bc19481d96933ec96cd27ade28c334215d53bafbab3e5d53`  
		Last Modified: Tue, 12 Jan 2021 05:15:59 GMT  
		Size: 31.7 MB (31749798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; 386

```console
$ docker pull mono@sha256:23a7d61d14921fb6cdac9af3089bbe43d4802f95e94f5783e68d8665d14f9ed8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99160096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1183437f303f6695f81fc122467d5294b0b29e6038bafbce0e5afb2e84dc8ac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:36 GMT
ADD file:601e9b729a871ae893eafa56eeac5d5d2c93a1bd60786560aae25b3644295a23 in / 
# Tue, 12 Jan 2021 00:39:36 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:56:09 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 03:56:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:56:56 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a5116b3c01b9daadc6c4605561821b0e7f908a2d339a79315de7651174cd76d7`  
		Last Modified: Tue, 12 Jan 2021 00:46:26 GMT  
		Size: 27.8 MB (27767991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae604efc877a26d5e9ef47c0ce73f76fc847780ddc3fc4f4fa2dae62aebc1b79`  
		Last Modified: Tue, 12 Jan 2021 04:02:20 GMT  
		Size: 255.8 KB (255850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5562f2f87a9508fba6e611a28b8bc7747b5368845e5cfa71f1a25a457f2c1e`  
		Last Modified: Tue, 12 Jan 2021 04:02:42 GMT  
		Size: 71.1 MB (71136255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:dcf3bae1c6fc5c089a7c08cc5d902422dbe8047387242a2f451937b6bc571788
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60139263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9427fdc99870b74f065955ba37c7bac20a528e45dd0092c6cd6f305c7181ea22`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:37:52 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 03:39:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:41:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a6b5cd501f71da14d37bddd625494e7a2de28217c260bc74553a9b4bc12b0f`  
		Last Modified: Tue, 12 Jan 2021 04:01:26 GMT  
		Size: 256.3 KB (256256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e85b5bce279ec9104f3a75e8c3a74fbd322ee4fff6244ab3046f12df7348d2a`  
		Last Modified: Tue, 12 Jan 2021 04:01:38 GMT  
		Size: 29.4 MB (29350170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10-slim`

```console
$ docker pull mono@sha256:e4a01967f524e646e2b249fab2be90f1c4939aa9acc0e33b7ebb914dea51284f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10-slim` - linux; amd64

```console
$ docker pull mono@sha256:c844ff3b7ee54eaba943c75712d14160804ef3ab8dabdc1e1c3272e74608a541
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94456820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1c7db5380987c54d84126cba76a6a6dccfaf004120eea20a3d79214279ab2d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 09:41:43 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 09:41:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 09:42:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e54505e49395a0d6a43f271952bf307a05153f6510a80ae27038c50df0efa46`  
		Last Modified: Tue, 12 Jan 2021 09:57:16 GMT  
		Size: 255.9 KB (255924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187e7566eb41f21ec1afcdd35f44280fdc2057d58a74789bd9affda7da2084a4`  
		Last Modified: Tue, 12 Jan 2021 09:57:29 GMT  
		Size: 67.1 MB (67092827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:c712f335d3056624b71f739eab72063f54dfdc9b1e79505f492350d575120386
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51670340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebaa3f292c5fd2c5f88f4c02fde89257131eddc5ecc1b5f4ab3aefb23f54cf7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:23 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cb1c784014fc8011ca8f4610f5131311b17486b9d6077606eaddacde5a2c27`  
		Last Modified: Tue, 09 Feb 2021 04:19:46 GMT  
		Size: 256.0 KB (256004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4b453be37d3b9ff06672c4a993a5489066cd5c2df5d33b2e6a60b32cadecdb`  
		Last Modified: Tue, 09 Feb 2021 04:19:58 GMT  
		Size: 26.6 MB (26575039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:1f06a597ee6d31d6be24bc45bd61b8bdbf82f41e4d20c6693c0562118c8c44d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48735200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9c6e0275747a42fb6d529c5e573d92cb73aed4ef196a5dd6421239f57cc5d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7698330b69a6c19085fab2ed78c48495acb00c18a4ffc6e0f6f40d54b9421b50`  
		Last Modified: Tue, 09 Feb 2021 04:19:18 GMT  
		Size: 256.0 KB (255991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44741965a508902c904fb46c6cdf26919ecb482fe42acc022eede0e3bab5e501`  
		Last Modified: Tue, 09 Feb 2021 04:19:28 GMT  
		Size: 25.8 MB (25775825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:6948940e8f06496863e933abbc4535ffbf2a6809be7a8ad57ba0472a7e425757
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57870227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48136d057bf03e9368936fd11090def9dea2ab83438eeb50225f1c3b77208e98`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 05:08:43 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 05:08:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 05:09:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6179e732b6b6a778fbe4321833a5ba71f60a206504e6a1a93efe345ec9aedf3e`  
		Last Modified: Tue, 12 Jan 2021 05:15:48 GMT  
		Size: 255.9 KB (255937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79964378e1ae7824bc19481d96933ec96cd27ade28c334215d53bafbab3e5d53`  
		Last Modified: Tue, 12 Jan 2021 05:15:59 GMT  
		Size: 31.7 MB (31749798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; 386

```console
$ docker pull mono@sha256:23a7d61d14921fb6cdac9af3089bbe43d4802f95e94f5783e68d8665d14f9ed8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99160096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1183437f303f6695f81fc122467d5294b0b29e6038bafbce0e5afb2e84dc8ac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:36 GMT
ADD file:601e9b729a871ae893eafa56eeac5d5d2c93a1bd60786560aae25b3644295a23 in / 
# Tue, 12 Jan 2021 00:39:36 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:56:09 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 03:56:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:56:56 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a5116b3c01b9daadc6c4605561821b0e7f908a2d339a79315de7651174cd76d7`  
		Last Modified: Tue, 12 Jan 2021 00:46:26 GMT  
		Size: 27.8 MB (27767991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae604efc877a26d5e9ef47c0ce73f76fc847780ddc3fc4f4fa2dae62aebc1b79`  
		Last Modified: Tue, 12 Jan 2021 04:02:20 GMT  
		Size: 255.8 KB (255850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5562f2f87a9508fba6e611a28b8bc7747b5368845e5cfa71f1a25a457f2c1e`  
		Last Modified: Tue, 12 Jan 2021 04:02:42 GMT  
		Size: 71.1 MB (71136255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:dcf3bae1c6fc5c089a7c08cc5d902422dbe8047387242a2f451937b6bc571788
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60139263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9427fdc99870b74f065955ba37c7bac20a528e45dd0092c6cd6f305c7181ea22`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:37:52 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 12 Jan 2021 03:39:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:41:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a6b5cd501f71da14d37bddd625494e7a2de28217c260bc74553a9b4bc12b0f`  
		Last Modified: Tue, 12 Jan 2021 04:01:26 GMT  
		Size: 256.3 KB (256256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e85b5bce279ec9104f3a75e8c3a74fbd322ee4fff6244ab3046f12df7348d2a`  
		Last Modified: Tue, 12 Jan 2021 04:01:38 GMT  
		Size: 29.4 MB (29350170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12`

```console
$ docker pull mono@sha256:188caea1633590c0af93df6462db94366998d465f4f654b3c6759b9ebf875dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12` - linux; amd64

```console
$ docker pull mono@sha256:e3c3faa1e0eccfec442341c7260bfb1faeccf40581fe8a00e77e794cf27d150b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235856726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d02da61afa912e62ef7cdc2e3b89fb6915716c72eccd75293b5c784ba17e5ce`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 09:40:56 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 09:41:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 09:41:33 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 09:48:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe02677df6f8831edfcea8a4558dcbb344dda0a234033ce403a445f71bb95e04`  
		Last Modified: Tue, 12 Jan 2021 09:56:50 GMT  
		Size: 255.9 KB (255924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6f0c1d36d945478bb94f4061ab9e9570a42d064b1bac55d482cc3d9eefdc1b`  
		Last Modified: Tue, 12 Jan 2021 09:57:04 GMT  
		Size: 67.1 MB (67079218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55acb8a81f9716f19bc8b425a4f2f9778868a086ced2c38a0d232c7e149e260b`  
		Last Modified: Tue, 12 Jan 2021 09:58:10 GMT  
		Size: 141.4 MB (141413515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v5

```console
$ docker pull mono@sha256:1d24028dba828fdc96b2b742b714f446f92b64abd6d180f3941954836178a989
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191752100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bcdc117695b526e00f4bac23d6c63d036306f5db62472b44bb3778d586032a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b88dcc371a0eb826a2922cd9da711f02c951f809c2d794f69ed376a2fece59`  
		Last Modified: Tue, 09 Feb 2021 04:20:55 GMT  
		Size: 140.1 MB (140107311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v7

```console
$ docker pull mono@sha256:c73416458bcb7bf5fa69488bd6815e282f46605e12f39a780d06ca20f5bc052d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187637328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808ec81fbec92ca5875883f0c5df523025c9784692513d2affb1e388dc139163`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195bce90b1707cb6f414c434f6348a2daa6c8bce4b713a9a1fa52e0d024305de`  
		Last Modified: Tue, 09 Feb 2021 04:20:29 GMT  
		Size: 138.9 MB (138939518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:bb8bcb03c776a1d69c8402a77aeb49e7302fca102ab82e11002ca319287ae33a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214424611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8b3b0d88c8a2f9826ad928f5035cd23a14395c38e57da6f376205bb25ac8d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 05:07:35 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 05:07:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 05:08:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 05:12:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c624bef28ff9228422eef122ec713693eb2e8d2ed78aa41f319bd0678a607c`  
		Last Modified: Tue, 12 Jan 2021 05:15:20 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ec950da6523b4cb54939edc61c6460d64327528adc05f607fbf005ff508a88`  
		Last Modified: Tue, 12 Jan 2021 05:15:34 GMT  
		Size: 31.7 MB (31720550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0470c4fa675956b4e41164ba69e70c7c53cbf56fa1fde6ca99247fd30d63182`  
		Last Modified: Tue, 12 Jan 2021 05:16:54 GMT  
		Size: 156.6 MB (156583646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; 386

```console
$ docker pull mono@sha256:3f6d7e510f3c7e210af3336de41288b7e8971519c559d7994389b5aaab7ca0d6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241641989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7d8ae0005ba40c7547dfff94755167dba0e74f722bd8583e10d292d8cc13d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:36 GMT
ADD file:601e9b729a871ae893eafa56eeac5d5d2c93a1bd60786560aae25b3644295a23 in / 
# Tue, 12 Jan 2021 00:39:36 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:55:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:55:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:56:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 03:59:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a5116b3c01b9daadc6c4605561821b0e7f908a2d339a79315de7651174cd76d7`  
		Last Modified: Tue, 12 Jan 2021 00:46:26 GMT  
		Size: 27.8 MB (27767991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ae7e24292b47c5c54d019f27f833b4d1fd06c6c1760426a915f4626d13ebb5`  
		Last Modified: Tue, 12 Jan 2021 04:01:42 GMT  
		Size: 255.9 KB (255867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f6fae6c251aafe4f2903014f5ca67d695cd2f74f87cc46b0b9b5e50650a9f`  
		Last Modified: Tue, 12 Jan 2021 04:02:03 GMT  
		Size: 71.1 MB (71105792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a6a59d3738ce8d2e6bad95e51859928eac584152411a872b1dfd4ec6cbffe4`  
		Last Modified: Tue, 12 Jan 2021 04:03:29 GMT  
		Size: 142.5 MB (142512339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; ppc64le

```console
$ docker pull mono@sha256:8cd03e8a315754c3631020ef221a2d0cbd0992577901c899c47ce5e69d61dd49
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203325644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be23bd3cc106fdd913dd4eff53c1f46dabb535e753abef0f566dae2c69eaea9d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:34:09 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:35:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:37:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 03:52:04 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e77824b16d99ee079aa03b8aabec031637265f7380c082326eaf48d078a93e7`  
		Last Modified: Tue, 12 Jan 2021 04:01:02 GMT  
		Size: 256.1 KB (256146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8e3bf2452dcba3a8621830f987ddbcc051bd5b6d5817e6d595c1cd93497f67`  
		Last Modified: Tue, 12 Jan 2021 04:01:08 GMT  
		Size: 29.3 MB (29311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be798b1b9507d975e13d056b87d688839b0f83115176be62486731bf9cac3ed7`  
		Last Modified: Tue, 12 Jan 2021 04:02:25 GMT  
		Size: 143.2 MB (143225573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0`

```console
$ docker pull mono@sha256:188caea1633590c0af93df6462db94366998d465f4f654b3c6759b9ebf875dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0` - linux; amd64

```console
$ docker pull mono@sha256:e3c3faa1e0eccfec442341c7260bfb1faeccf40581fe8a00e77e794cf27d150b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235856726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d02da61afa912e62ef7cdc2e3b89fb6915716c72eccd75293b5c784ba17e5ce`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 09:40:56 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 09:41:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 09:41:33 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 09:48:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe02677df6f8831edfcea8a4558dcbb344dda0a234033ce403a445f71bb95e04`  
		Last Modified: Tue, 12 Jan 2021 09:56:50 GMT  
		Size: 255.9 KB (255924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6f0c1d36d945478bb94f4061ab9e9570a42d064b1bac55d482cc3d9eefdc1b`  
		Last Modified: Tue, 12 Jan 2021 09:57:04 GMT  
		Size: 67.1 MB (67079218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55acb8a81f9716f19bc8b425a4f2f9778868a086ced2c38a0d232c7e149e260b`  
		Last Modified: Tue, 12 Jan 2021 09:58:10 GMT  
		Size: 141.4 MB (141413515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:1d24028dba828fdc96b2b742b714f446f92b64abd6d180f3941954836178a989
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191752100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bcdc117695b526e00f4bac23d6c63d036306f5db62472b44bb3778d586032a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b88dcc371a0eb826a2922cd9da711f02c951f809c2d794f69ed376a2fece59`  
		Last Modified: Tue, 09 Feb 2021 04:20:55 GMT  
		Size: 140.1 MB (140107311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:c73416458bcb7bf5fa69488bd6815e282f46605e12f39a780d06ca20f5bc052d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187637328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808ec81fbec92ca5875883f0c5df523025c9784692513d2affb1e388dc139163`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195bce90b1707cb6f414c434f6348a2daa6c8bce4b713a9a1fa52e0d024305de`  
		Last Modified: Tue, 09 Feb 2021 04:20:29 GMT  
		Size: 138.9 MB (138939518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:bb8bcb03c776a1d69c8402a77aeb49e7302fca102ab82e11002ca319287ae33a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214424611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8b3b0d88c8a2f9826ad928f5035cd23a14395c38e57da6f376205bb25ac8d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 05:07:35 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 05:07:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 05:08:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 05:12:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c624bef28ff9228422eef122ec713693eb2e8d2ed78aa41f319bd0678a607c`  
		Last Modified: Tue, 12 Jan 2021 05:15:20 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ec950da6523b4cb54939edc61c6460d64327528adc05f607fbf005ff508a88`  
		Last Modified: Tue, 12 Jan 2021 05:15:34 GMT  
		Size: 31.7 MB (31720550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0470c4fa675956b4e41164ba69e70c7c53cbf56fa1fde6ca99247fd30d63182`  
		Last Modified: Tue, 12 Jan 2021 05:16:54 GMT  
		Size: 156.6 MB (156583646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; 386

```console
$ docker pull mono@sha256:3f6d7e510f3c7e210af3336de41288b7e8971519c559d7994389b5aaab7ca0d6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241641989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7d8ae0005ba40c7547dfff94755167dba0e74f722bd8583e10d292d8cc13d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:36 GMT
ADD file:601e9b729a871ae893eafa56eeac5d5d2c93a1bd60786560aae25b3644295a23 in / 
# Tue, 12 Jan 2021 00:39:36 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:55:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:55:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:56:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 03:59:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a5116b3c01b9daadc6c4605561821b0e7f908a2d339a79315de7651174cd76d7`  
		Last Modified: Tue, 12 Jan 2021 00:46:26 GMT  
		Size: 27.8 MB (27767991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ae7e24292b47c5c54d019f27f833b4d1fd06c6c1760426a915f4626d13ebb5`  
		Last Modified: Tue, 12 Jan 2021 04:01:42 GMT  
		Size: 255.9 KB (255867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f6fae6c251aafe4f2903014f5ca67d695cd2f74f87cc46b0b9b5e50650a9f`  
		Last Modified: Tue, 12 Jan 2021 04:02:03 GMT  
		Size: 71.1 MB (71105792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a6a59d3738ce8d2e6bad95e51859928eac584152411a872b1dfd4ec6cbffe4`  
		Last Modified: Tue, 12 Jan 2021 04:03:29 GMT  
		Size: 142.5 MB (142512339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; ppc64le

```console
$ docker pull mono@sha256:8cd03e8a315754c3631020ef221a2d0cbd0992577901c899c47ce5e69d61dd49
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203325644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be23bd3cc106fdd913dd4eff53c1f46dabb535e753abef0f566dae2c69eaea9d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:34:09 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:35:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:37:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 03:52:04 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e77824b16d99ee079aa03b8aabec031637265f7380c082326eaf48d078a93e7`  
		Last Modified: Tue, 12 Jan 2021 04:01:02 GMT  
		Size: 256.1 KB (256146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8e3bf2452dcba3a8621830f987ddbcc051bd5b6d5817e6d595c1cd93497f67`  
		Last Modified: Tue, 12 Jan 2021 04:01:08 GMT  
		Size: 29.3 MB (29311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be798b1b9507d975e13d056b87d688839b0f83115176be62486731bf9cac3ed7`  
		Last Modified: Tue, 12 Jan 2021 04:02:25 GMT  
		Size: 143.2 MB (143225573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.107`

```console
$ docker pull mono@sha256:188caea1633590c0af93df6462db94366998d465f4f654b3c6759b9ebf875dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0.107` - linux; amd64

```console
$ docker pull mono@sha256:e3c3faa1e0eccfec442341c7260bfb1faeccf40581fe8a00e77e794cf27d150b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235856726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d02da61afa912e62ef7cdc2e3b89fb6915716c72eccd75293b5c784ba17e5ce`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 09:40:56 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 09:41:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 09:41:33 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 09:48:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe02677df6f8831edfcea8a4558dcbb344dda0a234033ce403a445f71bb95e04`  
		Last Modified: Tue, 12 Jan 2021 09:56:50 GMT  
		Size: 255.9 KB (255924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6f0c1d36d945478bb94f4061ab9e9570a42d064b1bac55d482cc3d9eefdc1b`  
		Last Modified: Tue, 12 Jan 2021 09:57:04 GMT  
		Size: 67.1 MB (67079218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55acb8a81f9716f19bc8b425a4f2f9778868a086ced2c38a0d232c7e149e260b`  
		Last Modified: Tue, 12 Jan 2021 09:58:10 GMT  
		Size: 141.4 MB (141413515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; arm variant v5

```console
$ docker pull mono@sha256:1d24028dba828fdc96b2b742b714f446f92b64abd6d180f3941954836178a989
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191752100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bcdc117695b526e00f4bac23d6c63d036306f5db62472b44bb3778d586032a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b88dcc371a0eb826a2922cd9da711f02c951f809c2d794f69ed376a2fece59`  
		Last Modified: Tue, 09 Feb 2021 04:20:55 GMT  
		Size: 140.1 MB (140107311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; arm variant v7

```console
$ docker pull mono@sha256:c73416458bcb7bf5fa69488bd6815e282f46605e12f39a780d06ca20f5bc052d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187637328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808ec81fbec92ca5875883f0c5df523025c9784692513d2affb1e388dc139163`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195bce90b1707cb6f414c434f6348a2daa6c8bce4b713a9a1fa52e0d024305de`  
		Last Modified: Tue, 09 Feb 2021 04:20:29 GMT  
		Size: 138.9 MB (138939518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:bb8bcb03c776a1d69c8402a77aeb49e7302fca102ab82e11002ca319287ae33a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214424611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8b3b0d88c8a2f9826ad928f5035cd23a14395c38e57da6f376205bb25ac8d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 05:07:35 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 05:07:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 05:08:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 05:12:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c624bef28ff9228422eef122ec713693eb2e8d2ed78aa41f319bd0678a607c`  
		Last Modified: Tue, 12 Jan 2021 05:15:20 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ec950da6523b4cb54939edc61c6460d64327528adc05f607fbf005ff508a88`  
		Last Modified: Tue, 12 Jan 2021 05:15:34 GMT  
		Size: 31.7 MB (31720550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0470c4fa675956b4e41164ba69e70c7c53cbf56fa1fde6ca99247fd30d63182`  
		Last Modified: Tue, 12 Jan 2021 05:16:54 GMT  
		Size: 156.6 MB (156583646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; 386

```console
$ docker pull mono@sha256:3f6d7e510f3c7e210af3336de41288b7e8971519c559d7994389b5aaab7ca0d6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241641989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7d8ae0005ba40c7547dfff94755167dba0e74f722bd8583e10d292d8cc13d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:36 GMT
ADD file:601e9b729a871ae893eafa56eeac5d5d2c93a1bd60786560aae25b3644295a23 in / 
# Tue, 12 Jan 2021 00:39:36 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:55:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:55:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:56:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 03:59:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a5116b3c01b9daadc6c4605561821b0e7f908a2d339a79315de7651174cd76d7`  
		Last Modified: Tue, 12 Jan 2021 00:46:26 GMT  
		Size: 27.8 MB (27767991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ae7e24292b47c5c54d019f27f833b4d1fd06c6c1760426a915f4626d13ebb5`  
		Last Modified: Tue, 12 Jan 2021 04:01:42 GMT  
		Size: 255.9 KB (255867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f6fae6c251aafe4f2903014f5ca67d695cd2f74f87cc46b0b9b5e50650a9f`  
		Last Modified: Tue, 12 Jan 2021 04:02:03 GMT  
		Size: 71.1 MB (71105792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a6a59d3738ce8d2e6bad95e51859928eac584152411a872b1dfd4ec6cbffe4`  
		Last Modified: Tue, 12 Jan 2021 04:03:29 GMT  
		Size: 142.5 MB (142512339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; ppc64le

```console
$ docker pull mono@sha256:8cd03e8a315754c3631020ef221a2d0cbd0992577901c899c47ce5e69d61dd49
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203325644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be23bd3cc106fdd913dd4eff53c1f46dabb535e753abef0f566dae2c69eaea9d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:34:09 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:35:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:37:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 03:52:04 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e77824b16d99ee079aa03b8aabec031637265f7380c082326eaf48d078a93e7`  
		Last Modified: Tue, 12 Jan 2021 04:01:02 GMT  
		Size: 256.1 KB (256146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8e3bf2452dcba3a8621830f987ddbcc051bd5b6d5817e6d595c1cd93497f67`  
		Last Modified: Tue, 12 Jan 2021 04:01:08 GMT  
		Size: 29.3 MB (29311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be798b1b9507d975e13d056b87d688839b0f83115176be62486731bf9cac3ed7`  
		Last Modified: Tue, 12 Jan 2021 04:02:25 GMT  
		Size: 143.2 MB (143225573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.107-slim`

```console
$ docker pull mono@sha256:98b3b4c0466037662d5fdb1c4ebf5c9d444424e7f852bde229afeb33d0385254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0.107-slim` - linux; amd64

```console
$ docker pull mono@sha256:8769207b9677e6f3f0e95b6423c76cdfd5e450f6b32c051db7b91db5577d7e21
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94443211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348b7e1144c12af5295b3c38dd57ef1b5c6e171ee9409efbbe2bacd0c680eae5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 09:40:56 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 09:41:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 09:41:33 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe02677df6f8831edfcea8a4558dcbb344dda0a234033ce403a445f71bb95e04`  
		Last Modified: Tue, 12 Jan 2021 09:56:50 GMT  
		Size: 255.9 KB (255924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6f0c1d36d945478bb94f4061ab9e9570a42d064b1bac55d482cc3d9eefdc1b`  
		Last Modified: Tue, 12 Jan 2021 09:57:04 GMT  
		Size: 67.1 MB (67079218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8398b92c5c9ef1d23664c131cc481982d148088d6e42f84a8a0070ad44075388
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51644789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15784a653dc26ebe76aa4ee3d2579ec792b224fbe78e00ecf4e8198fdbd8ce18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:0a95ecd350ee8679ab79ea59d0e4988d3410469917f8c16e3c330acfc0dc0e88
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48697810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f18c744ee67ee6ee2cfd81cffcab55fde0eb2c114377b949cea02c6d2327c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:90a25ba70e6af84267801fd4cbeb308a72f614df951c6c33e9782e140e373538
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57840965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b69b6854e1856fe6d38217029a566ca928db10d685c520adb43f1ecd510f16d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 05:07:35 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 05:07:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 05:08:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c624bef28ff9228422eef122ec713693eb2e8d2ed78aa41f319bd0678a607c`  
		Last Modified: Tue, 12 Jan 2021 05:15:20 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ec950da6523b4cb54939edc61c6460d64327528adc05f607fbf005ff508a88`  
		Last Modified: Tue, 12 Jan 2021 05:15:34 GMT  
		Size: 31.7 MB (31720550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; 386

```console
$ docker pull mono@sha256:521020ecd687652f6d5c2e2de3a818db2510b049378854f835bfc7caa058746e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99129650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a612a9ed794b39d2f1751626f377d4fe36630334994f4e592e859b2370d5d37`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:36 GMT
ADD file:601e9b729a871ae893eafa56eeac5d5d2c93a1bd60786560aae25b3644295a23 in / 
# Tue, 12 Jan 2021 00:39:36 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:55:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:55:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:56:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a5116b3c01b9daadc6c4605561821b0e7f908a2d339a79315de7651174cd76d7`  
		Last Modified: Tue, 12 Jan 2021 00:46:26 GMT  
		Size: 27.8 MB (27767991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ae7e24292b47c5c54d019f27f833b4d1fd06c6c1760426a915f4626d13ebb5`  
		Last Modified: Tue, 12 Jan 2021 04:01:42 GMT  
		Size: 255.9 KB (255867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f6fae6c251aafe4f2903014f5ca67d695cd2f74f87cc46b0b9b5e50650a9f`  
		Last Modified: Tue, 12 Jan 2021 04:02:03 GMT  
		Size: 71.1 MB (71105792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:fe8b241787171b74a2fd43cd5f13bd303c637bf330e80f289245b9c27b8eb306
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60100071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638800145fd3d9c6b9e6088d6dd2118832963e6457e99a6a04bfd75078bebd50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:34:09 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:35:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:37:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e77824b16d99ee079aa03b8aabec031637265f7380c082326eaf48d078a93e7`  
		Last Modified: Tue, 12 Jan 2021 04:01:02 GMT  
		Size: 256.1 KB (256146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8e3bf2452dcba3a8621830f987ddbcc051bd5b6d5817e6d595c1cd93497f67`  
		Last Modified: Tue, 12 Jan 2021 04:01:08 GMT  
		Size: 29.3 MB (29311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0-slim`

```console
$ docker pull mono@sha256:98b3b4c0466037662d5fdb1c4ebf5c9d444424e7f852bde229afeb33d0385254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:8769207b9677e6f3f0e95b6423c76cdfd5e450f6b32c051db7b91db5577d7e21
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94443211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348b7e1144c12af5295b3c38dd57ef1b5c6e171ee9409efbbe2bacd0c680eae5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 09:40:56 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 09:41:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 09:41:33 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe02677df6f8831edfcea8a4558dcbb344dda0a234033ce403a445f71bb95e04`  
		Last Modified: Tue, 12 Jan 2021 09:56:50 GMT  
		Size: 255.9 KB (255924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6f0c1d36d945478bb94f4061ab9e9570a42d064b1bac55d482cc3d9eefdc1b`  
		Last Modified: Tue, 12 Jan 2021 09:57:04 GMT  
		Size: 67.1 MB (67079218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8398b92c5c9ef1d23664c131cc481982d148088d6e42f84a8a0070ad44075388
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51644789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15784a653dc26ebe76aa4ee3d2579ec792b224fbe78e00ecf4e8198fdbd8ce18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:0a95ecd350ee8679ab79ea59d0e4988d3410469917f8c16e3c330acfc0dc0e88
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48697810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f18c744ee67ee6ee2cfd81cffcab55fde0eb2c114377b949cea02c6d2327c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:90a25ba70e6af84267801fd4cbeb308a72f614df951c6c33e9782e140e373538
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57840965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b69b6854e1856fe6d38217029a566ca928db10d685c520adb43f1ecd510f16d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 05:07:35 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 05:07:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 05:08:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c624bef28ff9228422eef122ec713693eb2e8d2ed78aa41f319bd0678a607c`  
		Last Modified: Tue, 12 Jan 2021 05:15:20 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ec950da6523b4cb54939edc61c6460d64327528adc05f607fbf005ff508a88`  
		Last Modified: Tue, 12 Jan 2021 05:15:34 GMT  
		Size: 31.7 MB (31720550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; 386

```console
$ docker pull mono@sha256:521020ecd687652f6d5c2e2de3a818db2510b049378854f835bfc7caa058746e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99129650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a612a9ed794b39d2f1751626f377d4fe36630334994f4e592e859b2370d5d37`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:36 GMT
ADD file:601e9b729a871ae893eafa56eeac5d5d2c93a1bd60786560aae25b3644295a23 in / 
# Tue, 12 Jan 2021 00:39:36 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:55:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:55:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:56:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a5116b3c01b9daadc6c4605561821b0e7f908a2d339a79315de7651174cd76d7`  
		Last Modified: Tue, 12 Jan 2021 00:46:26 GMT  
		Size: 27.8 MB (27767991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ae7e24292b47c5c54d019f27f833b4d1fd06c6c1760426a915f4626d13ebb5`  
		Last Modified: Tue, 12 Jan 2021 04:01:42 GMT  
		Size: 255.9 KB (255867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f6fae6c251aafe4f2903014f5ca67d695cd2f74f87cc46b0b9b5e50650a9f`  
		Last Modified: Tue, 12 Jan 2021 04:02:03 GMT  
		Size: 71.1 MB (71105792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:fe8b241787171b74a2fd43cd5f13bd303c637bf330e80f289245b9c27b8eb306
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60100071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638800145fd3d9c6b9e6088d6dd2118832963e6457e99a6a04bfd75078bebd50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:34:09 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:35:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:37:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e77824b16d99ee079aa03b8aabec031637265f7380c082326eaf48d078a93e7`  
		Last Modified: Tue, 12 Jan 2021 04:01:02 GMT  
		Size: 256.1 KB (256146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8e3bf2452dcba3a8621830f987ddbcc051bd5b6d5817e6d595c1cd93497f67`  
		Last Modified: Tue, 12 Jan 2021 04:01:08 GMT  
		Size: 29.3 MB (29311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12-slim`

```console
$ docker pull mono@sha256:98b3b4c0466037662d5fdb1c4ebf5c9d444424e7f852bde229afeb33d0385254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12-slim` - linux; amd64

```console
$ docker pull mono@sha256:8769207b9677e6f3f0e95b6423c76cdfd5e450f6b32c051db7b91db5577d7e21
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94443211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348b7e1144c12af5295b3c38dd57ef1b5c6e171ee9409efbbe2bacd0c680eae5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 09:40:56 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 09:41:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 09:41:33 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe02677df6f8831edfcea8a4558dcbb344dda0a234033ce403a445f71bb95e04`  
		Last Modified: Tue, 12 Jan 2021 09:56:50 GMT  
		Size: 255.9 KB (255924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6f0c1d36d945478bb94f4061ab9e9570a42d064b1bac55d482cc3d9eefdc1b`  
		Last Modified: Tue, 12 Jan 2021 09:57:04 GMT  
		Size: 67.1 MB (67079218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8398b92c5c9ef1d23664c131cc481982d148088d6e42f84a8a0070ad44075388
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51644789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15784a653dc26ebe76aa4ee3d2579ec792b224fbe78e00ecf4e8198fdbd8ce18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:0a95ecd350ee8679ab79ea59d0e4988d3410469917f8c16e3c330acfc0dc0e88
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48697810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f18c744ee67ee6ee2cfd81cffcab55fde0eb2c114377b949cea02c6d2327c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:90a25ba70e6af84267801fd4cbeb308a72f614df951c6c33e9782e140e373538
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57840965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b69b6854e1856fe6d38217029a566ca928db10d685c520adb43f1ecd510f16d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 05:07:35 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 05:07:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 05:08:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c624bef28ff9228422eef122ec713693eb2e8d2ed78aa41f319bd0678a607c`  
		Last Modified: Tue, 12 Jan 2021 05:15:20 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ec950da6523b4cb54939edc61c6460d64327528adc05f607fbf005ff508a88`  
		Last Modified: Tue, 12 Jan 2021 05:15:34 GMT  
		Size: 31.7 MB (31720550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; 386

```console
$ docker pull mono@sha256:521020ecd687652f6d5c2e2de3a818db2510b049378854f835bfc7caa058746e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99129650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a612a9ed794b39d2f1751626f377d4fe36630334994f4e592e859b2370d5d37`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:36 GMT
ADD file:601e9b729a871ae893eafa56eeac5d5d2c93a1bd60786560aae25b3644295a23 in / 
# Tue, 12 Jan 2021 00:39:36 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:55:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:55:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:56:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a5116b3c01b9daadc6c4605561821b0e7f908a2d339a79315de7651174cd76d7`  
		Last Modified: Tue, 12 Jan 2021 00:46:26 GMT  
		Size: 27.8 MB (27767991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ae7e24292b47c5c54d019f27f833b4d1fd06c6c1760426a915f4626d13ebb5`  
		Last Modified: Tue, 12 Jan 2021 04:01:42 GMT  
		Size: 255.9 KB (255867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f6fae6c251aafe4f2903014f5ca67d695cd2f74f87cc46b0b9b5e50650a9f`  
		Last Modified: Tue, 12 Jan 2021 04:02:03 GMT  
		Size: 71.1 MB (71105792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:fe8b241787171b74a2fd43cd5f13bd303c637bf330e80f289245b9c27b8eb306
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60100071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638800145fd3d9c6b9e6088d6dd2118832963e6457e99a6a04bfd75078bebd50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:34:09 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:35:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:37:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e77824b16d99ee079aa03b8aabec031637265f7380c082326eaf48d078a93e7`  
		Last Modified: Tue, 12 Jan 2021 04:01:02 GMT  
		Size: 256.1 KB (256146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8e3bf2452dcba3a8621830f987ddbcc051bd5b6d5817e6d595c1cd93497f67`  
		Last Modified: Tue, 12 Jan 2021 04:01:08 GMT  
		Size: 29.3 MB (29311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6-slim`

```console
$ docker pull mono@sha256:98b3b4c0466037662d5fdb1c4ebf5c9d444424e7f852bde229afeb33d0385254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6-slim` - linux; amd64

```console
$ docker pull mono@sha256:8769207b9677e6f3f0e95b6423c76cdfd5e450f6b32c051db7b91db5577d7e21
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94443211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348b7e1144c12af5295b3c38dd57ef1b5c6e171ee9409efbbe2bacd0c680eae5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 09:40:56 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 09:41:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 09:41:33 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe02677df6f8831edfcea8a4558dcbb344dda0a234033ce403a445f71bb95e04`  
		Last Modified: Tue, 12 Jan 2021 09:56:50 GMT  
		Size: 255.9 KB (255924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6f0c1d36d945478bb94f4061ab9e9570a42d064b1bac55d482cc3d9eefdc1b`  
		Last Modified: Tue, 12 Jan 2021 09:57:04 GMT  
		Size: 67.1 MB (67079218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8398b92c5c9ef1d23664c131cc481982d148088d6e42f84a8a0070ad44075388
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51644789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15784a653dc26ebe76aa4ee3d2579ec792b224fbe78e00ecf4e8198fdbd8ce18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:0a95ecd350ee8679ab79ea59d0e4988d3410469917f8c16e3c330acfc0dc0e88
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48697810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f18c744ee67ee6ee2cfd81cffcab55fde0eb2c114377b949cea02c6d2327c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:90a25ba70e6af84267801fd4cbeb308a72f614df951c6c33e9782e140e373538
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57840965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b69b6854e1856fe6d38217029a566ca928db10d685c520adb43f1ecd510f16d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 05:07:35 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 05:07:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 05:08:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c624bef28ff9228422eef122ec713693eb2e8d2ed78aa41f319bd0678a607c`  
		Last Modified: Tue, 12 Jan 2021 05:15:20 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ec950da6523b4cb54939edc61c6460d64327528adc05f607fbf005ff508a88`  
		Last Modified: Tue, 12 Jan 2021 05:15:34 GMT  
		Size: 31.7 MB (31720550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:521020ecd687652f6d5c2e2de3a818db2510b049378854f835bfc7caa058746e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99129650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a612a9ed794b39d2f1751626f377d4fe36630334994f4e592e859b2370d5d37`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:36 GMT
ADD file:601e9b729a871ae893eafa56eeac5d5d2c93a1bd60786560aae25b3644295a23 in / 
# Tue, 12 Jan 2021 00:39:36 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:55:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:55:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:56:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a5116b3c01b9daadc6c4605561821b0e7f908a2d339a79315de7651174cd76d7`  
		Last Modified: Tue, 12 Jan 2021 00:46:26 GMT  
		Size: 27.8 MB (27767991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ae7e24292b47c5c54d019f27f833b4d1fd06c6c1760426a915f4626d13ebb5`  
		Last Modified: Tue, 12 Jan 2021 04:01:42 GMT  
		Size: 255.9 KB (255867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f6fae6c251aafe4f2903014f5ca67d695cd2f74f87cc46b0b9b5e50650a9f`  
		Last Modified: Tue, 12 Jan 2021 04:02:03 GMT  
		Size: 71.1 MB (71105792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:fe8b241787171b74a2fd43cd5f13bd303c637bf330e80f289245b9c27b8eb306
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60100071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638800145fd3d9c6b9e6088d6dd2118832963e6457e99a6a04bfd75078bebd50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:34:09 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:35:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:37:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e77824b16d99ee079aa03b8aabec031637265f7380c082326eaf48d078a93e7`  
		Last Modified: Tue, 12 Jan 2021 04:01:02 GMT  
		Size: 256.1 KB (256146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8e3bf2452dcba3a8621830f987ddbcc051bd5b6d5817e6d595c1cd93497f67`  
		Last Modified: Tue, 12 Jan 2021 04:01:08 GMT  
		Size: 29.3 MB (29311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:latest`

```console
$ docker pull mono@sha256:188caea1633590c0af93df6462db94366998d465f4f654b3c6759b9ebf875dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:latest` - linux; amd64

```console
$ docker pull mono@sha256:e3c3faa1e0eccfec442341c7260bfb1faeccf40581fe8a00e77e794cf27d150b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235856726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d02da61afa912e62ef7cdc2e3b89fb6915716c72eccd75293b5c784ba17e5ce`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 09:40:56 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 09:41:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 09:41:33 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 09:48:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe02677df6f8831edfcea8a4558dcbb344dda0a234033ce403a445f71bb95e04`  
		Last Modified: Tue, 12 Jan 2021 09:56:50 GMT  
		Size: 255.9 KB (255924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6f0c1d36d945478bb94f4061ab9e9570a42d064b1bac55d482cc3d9eefdc1b`  
		Last Modified: Tue, 12 Jan 2021 09:57:04 GMT  
		Size: 67.1 MB (67079218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55acb8a81f9716f19bc8b425a4f2f9778868a086ced2c38a0d232c7e149e260b`  
		Last Modified: Tue, 12 Jan 2021 09:58:10 GMT  
		Size: 141.4 MB (141413515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:1d24028dba828fdc96b2b742b714f446f92b64abd6d180f3941954836178a989
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191752100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bcdc117695b526e00f4bac23d6c63d036306f5db62472b44bb3778d586032a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b88dcc371a0eb826a2922cd9da711f02c951f809c2d794f69ed376a2fece59`  
		Last Modified: Tue, 09 Feb 2021 04:20:55 GMT  
		Size: 140.1 MB (140107311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:c73416458bcb7bf5fa69488bd6815e282f46605e12f39a780d06ca20f5bc052d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187637328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808ec81fbec92ca5875883f0c5df523025c9784692513d2affb1e388dc139163`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195bce90b1707cb6f414c434f6348a2daa6c8bce4b713a9a1fa52e0d024305de`  
		Last Modified: Tue, 09 Feb 2021 04:20:29 GMT  
		Size: 138.9 MB (138939518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:bb8bcb03c776a1d69c8402a77aeb49e7302fca102ab82e11002ca319287ae33a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214424611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8b3b0d88c8a2f9826ad928f5035cd23a14395c38e57da6f376205bb25ac8d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 05:07:35 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 05:07:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 05:08:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 05:12:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c624bef28ff9228422eef122ec713693eb2e8d2ed78aa41f319bd0678a607c`  
		Last Modified: Tue, 12 Jan 2021 05:15:20 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ec950da6523b4cb54939edc61c6460d64327528adc05f607fbf005ff508a88`  
		Last Modified: Tue, 12 Jan 2021 05:15:34 GMT  
		Size: 31.7 MB (31720550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0470c4fa675956b4e41164ba69e70c7c53cbf56fa1fde6ca99247fd30d63182`  
		Last Modified: Tue, 12 Jan 2021 05:16:54 GMT  
		Size: 156.6 MB (156583646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:3f6d7e510f3c7e210af3336de41288b7e8971519c559d7994389b5aaab7ca0d6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241641989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7d8ae0005ba40c7547dfff94755167dba0e74f722bd8583e10d292d8cc13d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:36 GMT
ADD file:601e9b729a871ae893eafa56eeac5d5d2c93a1bd60786560aae25b3644295a23 in / 
# Tue, 12 Jan 2021 00:39:36 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:55:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:55:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:56:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 03:59:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a5116b3c01b9daadc6c4605561821b0e7f908a2d339a79315de7651174cd76d7`  
		Last Modified: Tue, 12 Jan 2021 00:46:26 GMT  
		Size: 27.8 MB (27767991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ae7e24292b47c5c54d019f27f833b4d1fd06c6c1760426a915f4626d13ebb5`  
		Last Modified: Tue, 12 Jan 2021 04:01:42 GMT  
		Size: 255.9 KB (255867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f6fae6c251aafe4f2903014f5ca67d695cd2f74f87cc46b0b9b5e50650a9f`  
		Last Modified: Tue, 12 Jan 2021 04:02:03 GMT  
		Size: 71.1 MB (71105792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a6a59d3738ce8d2e6bad95e51859928eac584152411a872b1dfd4ec6cbffe4`  
		Last Modified: Tue, 12 Jan 2021 04:03:29 GMT  
		Size: 142.5 MB (142512339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:8cd03e8a315754c3631020ef221a2d0cbd0992577901c899c47ce5e69d61dd49
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203325644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be23bd3cc106fdd913dd4eff53c1f46dabb535e753abef0f566dae2c69eaea9d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:34:09 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:35:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:37:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jan 2021 03:52:04 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e77824b16d99ee079aa03b8aabec031637265f7380c082326eaf48d078a93e7`  
		Last Modified: Tue, 12 Jan 2021 04:01:02 GMT  
		Size: 256.1 KB (256146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8e3bf2452dcba3a8621830f987ddbcc051bd5b6d5817e6d595c1cd93497f67`  
		Last Modified: Tue, 12 Jan 2021 04:01:08 GMT  
		Size: 29.3 MB (29311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be798b1b9507d975e13d056b87d688839b0f83115176be62486731bf9cac3ed7`  
		Last Modified: Tue, 12 Jan 2021 04:02:25 GMT  
		Size: 143.2 MB (143225573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

```console
$ docker pull mono@sha256:98b3b4c0466037662d5fdb1c4ebf5c9d444424e7f852bde229afeb33d0385254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:slim` - linux; amd64

```console
$ docker pull mono@sha256:8769207b9677e6f3f0e95b6423c76cdfd5e450f6b32c051db7b91db5577d7e21
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94443211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348b7e1144c12af5295b3c38dd57ef1b5c6e171ee9409efbbe2bacd0c680eae5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 09:40:56 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 09:41:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 09:41:33 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe02677df6f8831edfcea8a4558dcbb344dda0a234033ce403a445f71bb95e04`  
		Last Modified: Tue, 12 Jan 2021 09:56:50 GMT  
		Size: 255.9 KB (255924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6f0c1d36d945478bb94f4061ab9e9570a42d064b1bac55d482cc3d9eefdc1b`  
		Last Modified: Tue, 12 Jan 2021 09:57:04 GMT  
		Size: 67.1 MB (67079218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8398b92c5c9ef1d23664c131cc481982d148088d6e42f84a8a0070ad44075388
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51644789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15784a653dc26ebe76aa4ee3d2579ec792b224fbe78e00ecf4e8198fdbd8ce18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:0a95ecd350ee8679ab79ea59d0e4988d3410469917f8c16e3c330acfc0dc0e88
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48697810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f18c744ee67ee6ee2cfd81cffcab55fde0eb2c114377b949cea02c6d2327c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:90a25ba70e6af84267801fd4cbeb308a72f614df951c6c33e9782e140e373538
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57840965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b69b6854e1856fe6d38217029a566ca928db10d685c520adb43f1ecd510f16d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 05:07:35 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 05:07:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 05:08:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c624bef28ff9228422eef122ec713693eb2e8d2ed78aa41f319bd0678a607c`  
		Last Modified: Tue, 12 Jan 2021 05:15:20 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ec950da6523b4cb54939edc61c6460d64327528adc05f607fbf005ff508a88`  
		Last Modified: Tue, 12 Jan 2021 05:15:34 GMT  
		Size: 31.7 MB (31720550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:521020ecd687652f6d5c2e2de3a818db2510b049378854f835bfc7caa058746e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99129650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a612a9ed794b39d2f1751626f377d4fe36630334994f4e592e859b2370d5d37`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:36 GMT
ADD file:601e9b729a871ae893eafa56eeac5d5d2c93a1bd60786560aae25b3644295a23 in / 
# Tue, 12 Jan 2021 00:39:36 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:55:14 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:55:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:56:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a5116b3c01b9daadc6c4605561821b0e7f908a2d339a79315de7651174cd76d7`  
		Last Modified: Tue, 12 Jan 2021 00:46:26 GMT  
		Size: 27.8 MB (27767991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ae7e24292b47c5c54d019f27f833b4d1fd06c6c1760426a915f4626d13ebb5`  
		Last Modified: Tue, 12 Jan 2021 04:01:42 GMT  
		Size: 255.9 KB (255867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f6fae6c251aafe4f2903014f5ca67d695cd2f74f87cc46b0b9b5e50650a9f`  
		Last Modified: Tue, 12 Jan 2021 04:02:03 GMT  
		Size: 71.1 MB (71105792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:fe8b241787171b74a2fd43cd5f13bd303c637bf330e80f289245b9c27b8eb306
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60100071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638800145fd3d9c6b9e6088d6dd2118832963e6457e99a6a04bfd75078bebd50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:34:09 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 12 Jan 2021 03:35:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jan 2021 03:37:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e77824b16d99ee079aa03b8aabec031637265f7380c082326eaf48d078a93e7`  
		Last Modified: Tue, 12 Jan 2021 04:01:02 GMT  
		Size: 256.1 KB (256146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8e3bf2452dcba3a8621830f987ddbcc051bd5b6d5817e6d595c1cd93497f67`  
		Last Modified: Tue, 12 Jan 2021 04:01:08 GMT  
		Size: 29.3 MB (29311088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
