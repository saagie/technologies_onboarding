FROM saagie/r-image:3.6.3-base-1.63.0_SDKTECHNO-77

COPY ressources/requirements-bin.txt .
RUN apt update -qq && cat requirements-bin.txt | xargs apt install -yqq --no-install-recommends \
    && rm -rf /var/lib/apt/lists/*;

# Install remaining packages from source
COPY ressources/requirements-src.R .
RUN Rscript requirements-src.R