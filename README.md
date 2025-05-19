An unhandled exception occurred while processing the request.
JsonException: A possible object cycle was detected. This can either be due to a cycle or if the object depth is larger than the maximum allowed depth of 32. Consider using ReferenceHandler.Preserve on JsonSerializerOptions to support cycles. Path: $.Invitations.Customer.Invitations.Customer.Invitations.Customer.Invitations.Customer.Invitations.Customer.Invitations.Customer.Invitations.Customer.Invitations.Customer.Invitations.Customer.Invitations.Customer.Id.

builder.Services.AddControllers()
    .AddJsonOptions(options =>
    {
        options.JsonSerializerOptions.ReferenceHandler = System.Text.Json.Serialization.ReferenceHandler.Preserve;
        // Optional: Set a reasonable max depth if needed
        options.JsonSerializerOptions.MaxDepth = 64;
    });
