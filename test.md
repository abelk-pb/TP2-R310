graph TD
    %% Définition des Acteurs
    Client([Client - Externe]):::externe
    Vendeur[Agent Vendeur - Interne]:::interne
    Financier[Service Financier - Interne]:::interne
    Secretariat[Secrétariat / Hotline - Interne]:::interne

    %% Flux d'informations basés sur le TD
    Client -- "1. Critères (villes, dates, budget)" --> Vendeur
    Vendeur -. "2. Catalogue & Packs circuits" .-> Client
    Client -- "3. Demande de personnalisation" --> Vendeur
    Vendeur -- "4. Devis détaillé (Prix/Remise)" --> Client
    Client -- "5. Accord + Infos personnelles" --> Vendeur
    Vendeur -- "6. Dossier (Attente paiement)" --> Financier
    Client -- "7. Règlement (Acompte ou Total)" --> Financier
    Financier -. "8. Facture / Reçu" .-> Client
    Financier -- "9. Confirmation du solde" --> Vendeur
    Vendeur -- "10. Pack Voyage (Billets, Bons)" --> Client
    Client -- "11. Demande d'assistance" --> Secretariat

    %% Styles pour GitHub
    classDef externe fill:#e1f5fe,stroke:#01579b,stroke-width:2px
    classDef interne fill:#fff3e0,stroke:#e65100,stroke-width:2px
