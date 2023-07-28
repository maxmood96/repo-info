## `debian:testing-backports`

```console
$ docker pull debian@sha256:490522c5a97c97f5cf3187f41ad4dd8e7cdfa9643283e50c23a6dd08b05baf05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:3be7f2ae8e72d846342c37a045586e9b66a65c13358a55fa50f789f4f8552f3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49596918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b94abc53341f94fb3cd012528642faead73bb5f2e3cb0148225636033e4b1f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:27:06 GMT
ADD file:232c5a22b11e6861c0419feb6529d7da6a1b93600f93db9ef865f2b1d8526e58 in / 
# Thu, 27 Jul 2023 23:27:06 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:27:10 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1c40f7ee433c5de1ea05b673e25cceef231449d9025fa7a0c84e238ec3fefce8`  
		Last Modified: Thu, 27 Jul 2023 23:33:16 GMT  
		Size: 49.6 MB (49596696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ff8deaffd80b0df693f26e9c697dd7006a7a91226b803a234d7509e4f406a1`  
		Last Modified: Thu, 27 Jul 2023 23:33:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:a884cf840fa10f517ea0636c783c9a71c97dfb28ef93bf1a08d3c79c348bd78d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47416094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2a97bc25a42a98d7e3c78c17b3f89550bf7d4043b4a6efd94070a21cee4d99`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:49:39 GMT
ADD file:e61386345ac9d64106773e98ed84f3b915e2b39eb7a49a7eb17083c6c1e80eb1 in / 
# Thu, 27 Jul 2023 23:49:39 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:49:43 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a4c370becd20e68c205b8ef9f7f32f145c0949e93a884900ad6adf7b0168ef38`  
		Last Modified: Thu, 27 Jul 2023 23:54:09 GMT  
		Size: 47.4 MB (47415867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd57aa5d5d80da3e6f5cd3cdfc9d62b3db5519f23e8fd9748b7bc66ef6aa247`  
		Last Modified: Thu, 27 Jul 2023 23:54:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:7a067a851f6c6e831bf907947760743b50f74ba24bf05aebb500f8d175550458
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45212448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a244da2a38e06703c7f74913da0dc15b340a2477690c9827a53a034ec0903e31`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Jul 2023 00:00:43 GMT
ADD file:8e91c920955d8ab2b3460a4cf3a13c192194e92d62f2b0214da91deed5300a72 in / 
# Fri, 28 Jul 2023 00:00:44 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:00:47 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ba4f9bbc21ba8269a01460490071c98f69efa5cdb87ffbdcdb01d6d0eae7feb6`  
		Last Modified: Fri, 28 Jul 2023 00:07:10 GMT  
		Size: 45.2 MB (45212224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3877047b18c3fe164aa2510e4f6e2993c4ba675015e5b30d6e9ffbed0af463`  
		Last Modified: Fri, 28 Jul 2023 00:07:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:404a17d82e26cc0016049bbffd06c9c00a7b5d453c5c57171f806c7d005df0a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49590417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c4c942c054d453ad4225081dc36c27d63ce7127f974ca9665c7b6dd3436469`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:44:30 GMT
ADD file:27d300d7a32ad7c583bcdddac9c62b912c34a4060ab2e715b96a36ceb352bab4 in / 
# Thu, 27 Jul 2023 23:44:31 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:44:33 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0b4b6f5dd0ddc72b36cf824f3ed742ae466080edfbbb17333be4f975c06093fc`  
		Last Modified: Thu, 27 Jul 2023 23:50:03 GMT  
		Size: 49.6 MB (49590194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871094aa156e3324e8470595a21c0ce3d70bcb99d1cb08f815c6237a5a9d0fef`  
		Last Modified: Thu, 27 Jul 2023 23:50:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:aa0b7f86ea958fbcd4a2fad49aaa121c844211dfae7209f691f619c4f76bc0b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50617771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98cc693cffa511da37d18e2eef3ae7be70da4f8a00c78e55be950064062d57a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:41:07 GMT
ADD file:d2e15ec7f2e32466b3e91e033833b1a437761f59ba2ea5cd2fe79ddd0ba08100 in / 
# Thu, 27 Jul 2023 23:41:08 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:41:10 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5ed196291da2ef9605cef9f26d9142c9b7b6db4c61bfc3fa124a20a9449e49fb`  
		Last Modified: Thu, 27 Jul 2023 23:47:45 GMT  
		Size: 50.6 MB (50617549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7989d8e4afa0adfceec728e9898e9c444c0adabe2137d384d2c4645c54aed9`  
		Last Modified: Thu, 27 Jul 2023 23:47:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:dbf230ef6e825cd9923d21ff80c5e8d79f81ec3ae39369c5f411d6b860cbc69c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49544645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0ff7b716b316d0a01a476f090fb4002e63fc677d250a7062c4a0d398cdfd52`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:16:50 GMT
ADD file:36edbb732310d3835fd2c6a536e1f062390bd62e09f5a3a65ef35063a1021d65 in / 
# Thu, 27 Jul 2023 23:16:55 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:17:08 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:983342dfcbeef28222cd08e6111464390f87d09531fb648e36e74419b1e3794d`  
		Last Modified: Thu, 27 Jul 2023 23:28:15 GMT  
		Size: 49.5 MB (49544418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4e78361a8dfba8c917901f84027ef13c9cebfa9d54d5475f6f535823cd68f0`  
		Last Modified: Thu, 27 Jul 2023 23:28:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:6957f29e0d320c8ac2860f9be1673eba42556e7f82d87497de0ba5e0f0aef1f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53583401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51c2269426aaa3467e8cd41465f76387ba8dbf493147e26c45fd88f94228ce0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:44 GMT
ADD file:1097cc2b8a1d0dc4c0c138509885cba995ea8e57aec72bb44c61ae10a1597c77 in / 
# Thu, 27 Jul 2023 23:25:47 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:25:52 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:131ae2bf0201dc28363a8c6f4442669eb10652bb0360afa95a3bf4c626d1ffc3`  
		Last Modified: Thu, 27 Jul 2023 23:33:36 GMT  
		Size: 53.6 MB (53583176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee502461dc106f7ce524ee91344f2433df200fe967db2df6983da25570ae348`  
		Last Modified: Thu, 27 Jul 2023 23:33:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:acf043bf08ca006990193fbe1a21eff6e60d9e1a02102395a582bdf5a7ae864d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48030139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47729d1abae64cdf026c29eba7f7d385def1252c26a8f55a8d66434da0f183c1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:49:21 GMT
ADD file:a8d1e30c4e5e0291c66bafdf280bc79c83095de8bf54454640c070b15601fa3b in / 
# Thu, 27 Jul 2023 23:49:24 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:49:32 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6e624ce4159e36b9aa509a79a03ee8df8adfb80d8d5b3f8b9f8d599651c1edd4`  
		Last Modified: Thu, 27 Jul 2023 23:54:14 GMT  
		Size: 48.0 MB (48029915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b411e1ac01856fec9f98f97976b64096d919891e68a76c22ea6095fbc8860a7`  
		Last Modified: Thu, 27 Jul 2023 23:54:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
